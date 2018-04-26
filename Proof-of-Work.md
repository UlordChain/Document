# A One-Way Function for Proof-of-Work  

In this paper, we present a one-way function H, which is friendly to CPU architectures, but NOT to GPUs, FPGAs or ASICs.  


## 1. Design of One-way Function H
### 1.1 Principles
In order to resist efficiently implementation on GPUs, FPGAs and ASICs, the design of H should satisfy following features:  
1. More memory size than common hash functions. Considering the cache size of CPUs, the memory size for H is 1MB.  
2. A lot of memory accesses in random mode.  
3. High serialization and control dependence to prevent parallel execution in the function.  
4. Using 16 different types of one-way function to increase the chip area for ASIC implementation.  

### 1.2 Design of One-way Function H  
We use following definitions in our paper:  
[Definition 1] One-Way function y=H(x), the output y is 256 bits.  
[Definition 2] One-Way function family hi，0≤i≤15. The input of each function is 256 bits, except h0, which can accept arbitrary length input. The output of each function is 256 bits.  
[Definition 3] Pseudorandom number generator. seed(uint48 s) sets the seed, and rand() returns random result in 48 bits. We choose linear congruential generator Xn+1 = (aXn + c) mod m,  n ≥0，where a =25214903917, c = 11, m = 248 (rand48() in glibc).  
[Definition 4] Working memory M with size of |M| bytes. We choose |M|=1M=220.  
[Definition 5] reduce_bit(x, y) to reduce input x to output in y bits. The length of x is l bits，satisfied with l≥y。x is expanded X to L bits, where L mod y =0 and X[L-1:l]=0. X is split into L/y segments in y bits. The output is XOR of all segments.  
[Definition 6] RRS(x, y) to rotate shift right x with y bits.  

The one-way function H includes three algorithms:   
1. Initialize the working memory M.  
2. Modify the content of M.  
3. Generate the output according to the content of M.  

**[Alg-1] Initialize the working memory M**  
Input  :  x  	The input of one-way function y=H(x)  
Output： M 	Working memory    
Parameters: K   To adjust the computation speed. Larger K implies faster.  
Variables:  
a, b  vectors in 32 bytes，a[c1:c2] means the content of a from c1 to c2  
i    32-bit unsigned integer  
1. a[0:31]=h0(x);   
2. loop, i from 0 to |M|/32-1 	//if |M|=1M, the loop count is 215  
2.1  if i mod K ≠0      	//K is a configurable parameter to adjust speed  
2.1.1   	b[0 : 7] = rand0()*xor*(rand0()<<16);   
2.1.2   	b[8 :15] = rand1()*xor*(rand1()<<16);   
2.1.3   	b[16:23]= rand2()*xor*(rand2()<<16);   
2.1.4   	b[24:31]= rand3()*xor*(rand3()<<16);  
2.1.5  	b[0 : 31]= RRS(b[0:31], reduce_bit(i,8));  
2.1.6  	M[32*i:32*i+31]=b[0:31];  
2.1.7   	a[0:31]= a[0:31] *xor* b[0: 31];  
2.2  else  
2.2.1   	t=reduce_bit(a[0:31],4);  
2.2.2   	a[0:31]=ht(RRS(a[0:31], reduce_bit(i,8)));  
2.2.3   	seed0(reduce_bit(a[ 0: 7],48)); 	seed1(reduce_bit(a[ 8:15],48));   
seed2(reduce_bit(a[16:23],48)); 	seed3(reduce_bit(a[24:31],48));  
2.2.4   M[32*i:32*i+31]= a[0:31];  



**Comment on Alg-1**  
This algorithm will generate the random content in |M| bytes for working memory. In step 2, 32 bytes will be generated in one loop. Consecutive K-1 blocks are generated from random generator (in step 2.1), and one block from one-way function family (in step 2.2). Because the speed of random generator is faster than one-way functions, increasing K can reduce the frequentness of calling one-way functions to increase the fulfill speed of working memory.  
In random fulfilling (from step 2.1.1 to 2.1.4), there are four independent generators to produce a 32-byte block with a rotate shift in variable bits (step 2.1.5). Two factors determine the content of the 32-byte block: 1) Four 48-bit seeds; 2) loop control variable i. So the number of all possible input to fulfill one block is 296+15=2111.  
When calling one-way function (step 2.2.2), whose input depend on latest output of one-way function and the content of previous K-1 blocks (step 2.1.7). It results in the computation of one-way function must be followed random fulfill.  The number of all possible input of one-way function is 2256+8=2264.  
In step 2.2.3, the seeds of four generators are updated according to the output of the one-way function. It requires that the following random fulfill must run after one-way function.  
It can be seen that alg-1 is satisfied: 1) execution sequentially; 2) impossible to predict the content of one block.  

**Alg-1 flow chart**    
![image](https://github.com/binbinErices/Car_CRM_System/blob/master/img/1.png?raw=true)

**[Alg-2] Modify Working Memory**  
Input  :   M    Working memory  
Output：  M 	Working memory  
          c     32-byte array to alg-3  
Parameters:   
L   To balance the execution time between memory access and calling one-way functions  
C   To adjust the number of round, no less than |M|/128  
Variables:  
s, t1, t2: 8-bit unsigned integer; i: 32-bit unsigned integer; r: 64-bit unsigned integer;  
b: 64-byte array; a: 32-byte array   
1. a[0:31]=c[0:31]=h0(M[|M|-32:|M|-1]); r=reduce_bit(a[0:31], 64);	//hash the last block of M  
2. Loop, i from 0 to C      	
2.1   seed(reduce_bit(a[0:31], 48)); 		//Initialize random generator  
2.2   Loop, j from 0 to 64*L-1  				
2.2.1    base=(rand()+r) mod 264; offset= (reduce_bit(r,8)<<8)+1;   //random memory address  
2.2.2    addr1=(base-offset) mod |M|; addr2=(base+offset) mod |M|  
2.2.3    t1=M[addr1];		t2=M[addr2];  	s=a[j mod 32];  
2.2.4    M[addr1]= t2 *xor* s;  	M[addr2]= t1 *xor* s; 	b[j mod 64]=t1 *xor* t2;		//Modify M 
2.2.5    r=(r+s+t1+t2) mod 264;  					
2.3   t=reduce_bit(r,4);  
2.4   a[0:31]=reduce_bit(b[0:63], 256);  
2.5   a[0:31]=ht(RRS(a[0:31], reduce_bit(i+r,8)));  
2.6   c[0:31]=c[0:31] *xor* a[0:31]  

**Comment on Alg-2**  
The first step of the algorithm obtains the hash result of last block of M, which requires the completion of Alg-1 before this algorithm can be executed, ensuring the sequence of the two algorithms.  
The core of the algorithm is the step 2, the main purpose of which is to modify the contents of M randomly. Divided into two phases: 1) randomly modify the contents of the memory according to the parameters (2.1 to 2.2 steps); 2) use the one-way function family according to the sorted contents to regenerate the memory modification parameters.  
In the memory modification phase, each time 2 bytes of M are modified. The addresses are determined by a, the result of the last one-way function, and r, where r (step 2.2.5) depends on the value of all previous memory accesses and the result of a one-way function. In each loop of step 2.2, two memory access addresses are generated, and their difference is 2×offet+2. Since the lower 8 bits of offset are 0, if the offset is not equal to 0, the gap between them is more than 512 bytes. At this time, the two memory accesses will not fall in the same cache line. When reduce_bit(r,8) is greater than 4, the gap between the two is more than 2K, where 2KB is often a storage line size of DRAM. This makes it likely that two memory accesses are not in one memory row, but there is also a possibility in one memory row to increase the complexity of the ASIC memory system design. In step 2.2.4, the XOR method is used to cross-over the content of the two memories and the contents of the one-way function, thus maintaining the randomness of the original content.  
The one-way function input of step 2.5 depends on the memory access contents of the current cycle, the current loop number i, and r (including the history information of the previous execution process of the algorithm).  
Step 2.6 fuse the execution information of all the one-way functions in c as the random number input of the subsequent algorithm.  

**Alg-2 flow chart**    
![image2](https://github.com/binbinErices/Car_CRM_System/blob/master/img/2.png?raw=true)  

**[Alg-3] Generate output based on working memory**  
Input  :   M 	Working memory  
          c     32-byte array from alg-2  
Output:    y     256-bit result  
Parameters:   
D   To adjust the number of calculations for a one-way function.   
1. y[0:31]=c[0:31]; i=0;  
2. Loop  
2.1   t= reduce_bit(y[0:31],4);  
2.2   d=reduce_bit(y[0:31], D)+1;   
2.3   Loop, j from 0 to d             //At least once  	  					
2.3.1    y[0:31]=y[0:31] *xor* M[32*i, 32*i+31];  
2.3.2    i++;  
2.3.3    if i =|M|/32-1 then  
2.3.3.1     y[0:31]=h0(RRS(y[0:31], reduce_bit(i+t,8))); return  
2.4   y=ht(RRS(y[0:31], reduce_bit(i+t,8)));  

**Comment on Alg-3**  
The main purpose of this algorithm is to quickly produce the final result based on the contents of working memory M, accessing M in a sequential order with 32-byte block. In step 2.3, the result of the last one-way function is overlaid with the contents of the d blocks. d is a random value that depends on the result of the last one-way function and is between 0 and 2D-1. There is the possibility of parallel computing here, but since the initial i and d in 2.3 steps cannot be predicted in advance, it will undoubtedly increase the difficulty of judgment.  
The one-way function calculation in step 2.4 adds the factor of the loop variable i, so that its input depends not only on y but also on the position of the loop. Through step 2.3.1, the input of the one-way function contains information of all memory contents.  
Step 2.3.3.1 determines that the one-way function h0 must be performed in the final step of the algorithm.  
 
**Alg-3 flow chart**  
![image3](https://github.com/binbinErices/Car_CRM_System/blob/master/img/3.png?raw=true)  

### 1.3 Operations in Function H
The operations in three algorithms of one-way function H are described in table 1-1.    
**Table 1-1 Operations in One-Way Function H  **    
    
 
| #alg | Calling one-way function family | Working memory access |  
| -------- |--------------|---------|  
| alg-1 | \|M\|/32K | \|M\|/32 256-bit memory write operations | 
| alg-2 | C | 128CL 8-bit memory read operations 128CL 8-bit memory read operations |  
| alg-3 | \|M\|/(32*2D-1) | \|M\|/32 256-bit memory read operations |   

 **Parameter configuration: |M|=1M, K=128, L=4, C=512, D=8**
 
### 1.4 One-way Function Family  
One-way function family is described in table 1-2 and 1-3.  
**Table 1-2 One-way Function Family**  

|  t  | Type | Function Name | Source code |  
| --  | -------- |--------------|---------|  
| 0 | SHA-3 | SHA3-256 |OpenSSL | 
| 1 | SHA-1 | SHA-1 | OpenSSL |  
| 2 | SHA-2 | SHA-256|OpenSSL | 
| 3 | SHA-2 | SHA-512 |OpenSSL | 
| 4 | Whirlpool |Whirlpool| OpenSSL |  
| 5 | RIPEMD | RIPEMD-160 | OpenSSL | 
| 6 | BLAKE2 | BLAKE2s(256bits) |OpenSSL | 
| 7 | AES | AES(128bits) | OpenSSL |  
| 8 | DES | DES | OpenSSL | 
| 9 | RC4 | RC4 |OpenSSL | 
| 10 | Camellia | Camellia(128bits) | OpenSSL |  
| 11 | CRC | CRC32 | JTR | 
| 12 | HMAC | HMAC(MD5) |OpenSSL | 
| 13 | GOST | GOST R 34.11-94 | JTR |  
| 14 | HAVAL | HAVAL-256/5|JTR | 
| 15 | Skein | Skein-512(256bits) |JTR |   


**Table 1-3 Implementation Detail of One-way Function Family**
```
1.	1. SHA1 
2.	$hash[ 0:19] = sha1($input)  
3.	$hash[20:39] = sha1(~$input)  // ~为按字节取反
4.	$output[0:31] = reduce_bit(hash[0:39], 256) 
5.	  
6.	2. SHA256 
7.	$output[0:31] = sha256($input)  
8.	  
9.	3. SHA512  
10.	$hash[0:63] = sha512($input) 
11.	$output[0:31] = reduce_bit(hash[0:63], 256)
12.	  
13.	4. SHA3-256  
14.	$output[0:31] = sha3-256($input)  
15.	  
16.	5. Whirlpool  
17.	$hash[0:63] = whirlpool($input)  
18.	$output[0:31] = reduce_bit($hash[0:63], 256)
19.	  
20.	6. RIPEMD-160 
21.	$hash[ 0:19] = ripemd160($input)  
22.	$hash[20:39] = ripemd160(~$input)  
23.	$output[0:31] = reduce_bit(hash[0:39], 256) 
24.	  
25.	7. BLAKE2s(256bits)  
26.	$output[0:31] = blake2s($input)  
27.	  
28.	8. AES(128bits)  
29.	$hash[0:31] = sha256($input)  
30.	$hash2[0:15] = md5($hash[0:31])  
31.	$key = aes128_set_key($hash2[0:15])  
32.	$output[ 0:15] = aes128_encrypt($key, $hash[ 0:15])  
33.	$output[16:31] = aes128_encrypt($key, $hash[16:31])
34.	  
35.	9. DES  
36.	$hash[0:31] = sha256($input)  
37.	$hash2[0:15] = md5($hash[0:31])  
38.	$key = DES_set_key_unchecked($hash2[0:15])  
39.	$output[ 0: 7] = DES_encrypt($key, $hash[ 0: 7])
40.	$output[ 8:15] = DES_encrypt($key, $hash[ 8:15])
41.	$output[16:23] = DES_encrypt($key, $hash[16:23])
42.	$output[24:31] = DES_encrypt($key, $hash[24:31])
43.	  
44.	10. GOST R 34.11-94  
45.	$output[0:31] = gost($input)  
46.	  
47.	11. HAVAL-256/5  
48.	$output[0:31] = haval5_256($input)  
49.	  
50.	12. Skein-512(256bits)  
51.	$output[0:31] = skein512_256($input)  
52.	  
53.	13. CRC32  
54.	$hash[0:31] = sha256($input)  
55.	$output[0:31] = crc32($hash[0:31]) 
56.	  
57.	14. HMAC(MD5)  
58.	$hash[0:15] = hmac_md5($input, $input)   
59.	$output[0:31] = sha256($hash[0:15])  
60.	  
61.	15. Camellia(128bits)  
62.	$hash[0:31] = sha256($input)  
63.	$hash2[0:15] = md5($hash[0:31])  
64.	$key = Camellia_set_key($hash2[0:15])  
65.	$output[ 0:15] = Camellia_encrypt($key, $hash[ 0:15])  
66.	$output[16:31] = Camellia_encrypt($key, $hash[16:31])
67.	  
68.	16. RC4(256bits) 
69.	$hash[0:31] = sha256($input)  
70.	$hash2[0:15] = md5($hash[0:31]) 
71.	$key = RC4_set_key($hash2[0:15])  
72.	$output[0:31] = RC4($key, $hash[0:31]) 

```

### 1.5 Output of One-way Function H  
Standard output of H  
H(“0123456789”)= cb98c372548618317a2dc286a7481701e5ea94892c9eb371d932c83d94ddd459    
H(“HelloWorld”)= 8d184a295c91aa46243c64452c0417fcff4d5ea67b30d43dd1e5a358171b9929    

Calling function H consecutively as following:  
xi+1=H(xi)  x0=“”  i=1…106  
Assemble all xi to obtain a 32MB bit stream Y.  
Using NIST random test tool ，test Y’s frequency and runs. Results are presented in table 1-3. All P-values are greater than 0.01. So, the bit stream Y (function H) is pass the random test.  

**Table 3-1 Random Test for Function H**  

Test Item | P-value
 --- | ------
Frequency | 0.859141
Runs	| 0.876262  


## 2. Performance of One-way Function H   
### 2.1 Performance on CPU  
**CPU Platforms**  
Our test is based on four platforms, including server, PC, Tianhe-2, and embedded system. The parameters of these platforms are presented in table 2-1.  
**Table 2-1 CPU Platforms**  

|  Platforms  | #1 Server | #2 PC | #3 Tianhe-2 | #4 Embedded System|  
| -------- | -------- | -------------- | --------- | ---------- |  
| Processor | E5-2609 | Core i5 7500 |E5-2692 v2 | TX1 |  
| Micro-architecture | Haswell | Kaby Lake | Ivy Bridge |A57|  
| SIMD | SSE 2/3/4.1/4.2AVX/AVX2 |SSE 2/3/4.1/4.2AVX/AVX2|SSE 2/3/4.1/4.2AVX |NEON |  
| Cores | 2*6 | 4 | 2*12 | 4 |  
| Hyper Thread | Nonsupport | Nonsupport |Support |Nonsupport |  
| Frequency | 1.9 GHz | 3.4 GHz | 2.20GHz |2.1GHZ|  
| Memory size | 64 GB | 8 GB |64 GB | 2GB |  
| L1 Cache Size/per core | 32 KB+32 KB | 32 KB+32 KB | 32 KB+32 KB |32 KB+32 KB|  
| L2 Cache/per core | 256 KB | 256 KB |256 KB | 2MB（shared） |  
| L3 Cache | 15MB | 6MB | 30MB | |  
| Operating System | CentOS 6.6（64 bits） | Windows 10（64 bits）|Red Hat Enterprise 6.2 | Ubuntu 14.04 LTS |  
| Compiler | gcc7 (GCC) 7.1.0 |Microsoft VS2015 C/C++ 19.00.24215.1 | icc 14.0.2 | |  


**Performance of One-Way Function Family**  
Performance of 16 one-way functions on platform 1,2 and 3 are described in table 2-2.  

---

**Table 2-2 Throughput of One-Way Function Family(Mps)**  

| t | Type | Function Name | Server | PC | Tianhe-2|  
| -- | ------- |------------|-----|-----|----|    
| 0 | SHA-3 | SHA3-256 | 1.01 | 1.28 | 1.02 |  
| 1 | SHA-1 | SHA-1 | 2.15 | 4.51 | 3.19 |   
| 2 | SHA-2 | SHA-256 | 2.81 | 5.26 | 3.72 | 
| 3 | SHA-2 | SHA-512 | 1.34 | 3.68 | 2.54 |  
| 4 | Whirlpool | Whirlpool |	0.92 | 2.43 | 1.50 |   
| 5 | RIPEMD | RIPEMD-160 | 0.95 | 1.51 | 1.46 |  
| 6 | BLAKE2 | BLAKE2s(256bits) | 1.66 | 2.42 | 2.48 |  
| 7 | AES	| AES(128bits) | 0.92 | 1.79 |  1.28 | 
| 8 | DES | DES | 0.66 | 1.25 | 0.91 |   
| 9 | RC4 | RC4 | 0.72 | 1.42 | 1.06 |  
| 10 | Camellia | Camellia(128bits) | 1.07 | 2.04 | 1.52 |   
| 11 | CRC | CRC32 | 2.16 | 3.98 | 2.94 |   
| 12 | HMAC | HMAC(MD5) | 0.47 | 0.66 | 0.67 |    
| 13 | GOST | GOST R 34.11-94 | 0.37 | 0.73 | 0.50 |   
| 14 | HAVAL | HAVAL-256/5 | 1.67 | 2.43 | 1.81 |  
| 15 | Skein | Skein-512(256bits）| 2.17 | 4.47 | 3.17 |  

**In this table, the function with highest throughput is SHA256, the lowest is GOST or HMAC. The highest throughput is 7.5~8.0 times as the lowest one.**  

**Execution Time Distribution**  
With one core on server platform, the execution time distribution of H is described as table 2-3.  
**Table 2-3 Execution Time Distribution of H**  

|     | Alg-1 Initialize Memory|Alg-2 Modify Memory (Step 2.2)| Alg-2 Calling One-way Functions (Step 2.5)| Alg-3 Generate Result |  
|--|------|------|------|------|  
| Distribution | 36% | 53% | 1% | 10% |  

**The execution time of function H concentrates on modification memory in alg-2.**

**Performance of One-way function H**    
Table 2-4 and figure 2-1 show the performance of one-way function H on different performance. The thread number with the highest performance exactly is equal to the number of the cores.     
**Table 2-4 Throughput of One-way Function H on Different Platforms (hashes per second)**  

| Number of Threads | 1 | 4 | 8 | 12 | 16 | 24 | 32 | 48 | 64 |  
|----|---|---|---|---|---|---|---|----|---|    
| Server | 80 | 315 | 628 | 938 | 837 | 836 | 867 | 858 | 763 |  
| PC | 168 | 641 | 634 | 631 | 633 | 629 | 627 | 625 | 625 |  
| Tianhe-2 | 115 | 443 | 797 | 1186 | 1578 | 2337 | 2208 | 2177 | 2171 |  
| Embedded System | 73 | 138 | 133 | 133 | 133| 133 | 133 |	132 | 133 |  

![image4](https://github.com/binbinErices/Car_CRM_System/blob/master/img/2-1.png?raw=true)  
**Figure 2-1 Throughput of One-way Function H on Different Platforms(hashes per second)**  


### 2.2 Performance on GPUs  
Our test is based on Mainstream consumer-level graphics: GTX 1080, GTX Titan X. Their specification is shown in table 2-5.  

**Table 2-5 Specification of GPUs**  

| GPU |GTX 1080|GTX Titan X|  
|---|---|----|  
|Micro-architecture|Pascal|Maxwell|  
|Number of Cores| 2560 | 3072 |  
| Frequency| 1.6GHZ | 1.0GHZ |  
| Memory Size | 8GB | 12GB |  
|Memory Width | 256-bits | 384-bits |  
|Memory Bandwidth| 320GBps | 336GBps |  
|Power Consumption | 180W | 250W |  


#### 1. Constraint on Number of Simultaneous Threads  
Because of the limitation of memory size on GPU, only 4 Kilo one-way functions can be executed simultaneously, occupying 4GB memory.
There is no obvious parallelism within the three main algorithms in function H, so it is difficult to execute a one-way function H at the same time by multiple threads, and only one one-way function can be executed by one thread.  
At this point, there are a total of 4K threads on one GPU. This will lead to the first constraint: the number of threads that can be executed in parallel is too small and overall parallelism is limited.  

####  2. Constraint on SMT  
The GPUs use SIMT (Single Instruction Multithreading) method, where one Warp (=32) threads execute the same instruction. In the case of a branch instruction, if the execution paths between the threads are different, all the paths of each thread need to be executed serially, respectively, until all threads in one Warp execute to the same path.  
In our one-way function H, it will choose one from 16 one-way functions randomly. And the number of cycles varies between 1 and 2D-1 depending on the input data in step 2.3 of Alg-3. This will cause the threads on the GPU to execute different paths so that different threads can only execute serially, thereby suppressing the parallelism of the GPU.  

#### 3. Constraint on Memory Access   
In Alg-2, the access unit to the working memory M is byte, and the address is highly random. Since the GPU on-chip cache has a very limited capacity, the memory access in Alg-2 basically needs to be read from the video memory. Although the memory width of GPU is up to 256 bits (or even 384 bits), it is only valid for ONE byte, which makes the GPU memory access bandwidth only 3% utilization.  
Due to the large number of reliance on memory accesses, the latency of memory access instructions can be as long as several hundred cycles, and because of the small number of threads, it is difficult to cover the long latency of these memory access instructions.  

**Performance**  
Table 2-6 and Figure 2-2 show the performance on the GTX 1080 and GTX Titan X.  

**Table 2-6 Throughput of One-way Function H on Different GPUs**  
(hashes per second，Single card, thread set to 4096)  
![image5](https://github.com/binbinErices/Car_CRM_System/blob/master/img/4.png?raw=true)  

![image6](https://github.com/binbinErices/Car_CRM_System/blob/master/img/2-2.png?raw=true)  
**Figure 2-2 Throughput of One-way Function H on Different GPUs(hashes per second)**  

In Figure 2-2, although the number of cores of 1080 is significantly less than Titan X, its performance is significantly improved. This may be because the former adopts more sophisticated architecture Pascal, which is the previous Maxwell architecture. The two-generation architecture has a significant difference to this one-way function algorithm:  
On 1080, performance continues to increase as the number of simultaneous one-way functions is increased. However, since only 8GB of memory is available, the maximum number of one-way functions that can be calculated simultaneously is only 4K (4GB of memory is used).
On Titan X, when the number of simultaneous calculations of a one-way function increases by more than 2K, the performance is severely degraded, which may be related to its internal design approach to memory access.  
Compared with Figure 2-1, the performance of 1080 is basically equivalent to that of a general server.  



 
 


