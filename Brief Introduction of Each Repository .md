# Brief Introduction of Each Repository of Ulord  

Ulord is a public blockchain on which various types of digital resource application scenarios including text, pictures, music, video and software can be loaded. It consists of 24 repositories, from the basic chain, sidechian, crosschain, node-multi-hashing to wallet, ulordrig. The following are the brief introductions of each repository for you to get a quick understanding of Ulord source code. 

## 1. UlordChain 
Ulord is a P2P value delivery public chain. Through building its blockchain underlying architecture and digital resource distribution protocols, it enables third-party developers to explore their own applications over open-source agreements to form a complete ecology of blockchain technology and applications. Based on various rules and protocols created by Ulord, it loads various types of digital resource application scenarios including text, pictures, music, video and software, providing a direct docking platform for information creators and consumers.

## 2. Ulordj-thin 
The ulordj library is a Java implementation of the Ulord protocol, which allows it to maintain a wallet and send/receive transactions without needing a local copy of Ulord Core. It comes with full documentation and some example apps showing how to use it. USC made a "thin" version of ulordj including just the components needed by the USC node.

## 3. Ulord-Sidechain 
Ulord-Sidechain a.k.a USC is a Secondary chain for Ulord implemented in java. USC's goal is to provide value and functionality to the Ulord ecosystem by enabling smart-contracts, near instant payment confirmations and higher-scalability. USC smart contract platform supports 2-way peg with Ulord that also rewards Ulord miners via merge-mining, allowing them to actively participate in the Smart Contract revolution.

## 4. gradle-witness 
Gradle Witness is a gradle plugin that enables static verification for remote dependencies that are included into the project. i.e The author of the project can include dependency verfification to verify the integrity of the project dependencies.

## 5. node-multi-hashing
This project provides a proof of work (POW) algorithm that can work efficiently on CPU but is difficult to implement efficiently on GPU, FPGA, and ASIC. The way to achieve this is to limit the work efficiency on the GPU, FPGA, and ASIC through high memory limitations, high degree of serialization, large control of correlation, combination of multiple hash functions, and full use of the CPU's SIMD instructions.

## 6. CrossChain
The project of Ulord CrossChain is a tool that allows for the exchange of one cryptocurrency for another without the need for a trusted third party. Ulord CrossChain tool uses a hash time-locked smart contract so that a party must deliver the currency to be swapped within a specified time, or else the transaction will be cancelled. Your chain can be used so long as it supports OP_SHA256 and OP_CHECKLOCKTIMEVERIFY.

7.	cryptohello-hash-lib 
This project is a tool for packaging a proof of work (POW) algorithm used by Ulord into a static data link library and a dynamic link library file for use by Python.

8.	Uwallet-client-pro 
The light wallet is based on "Simplified Payment Verification" (SPV). The user only needs to save all the block headers, the wallet can be verified for payment even if not all the nodes are operating. The user does not need to verify the transaction himself. The wallet can find a matching transaction from somewhere in the blockchain and determine that the network has approved the transaction and how many blocks have been confirmed.

9.	Uwallet-server 
Ulord wallet server, which stores UTXO, transaction history, and on-chain data, is used to quickly interact with the light wallet and the underlying blockchain.

10.	Uwallet
Uwallet is an abstract interface based on spv wallet, which can provide a call interface for wallets of each business layer to separate wallet from business and reduce program coupling.


11.	uwallet-client
It is used for sending and receiving ULD. You can download and install it directly. It is the simplified version of SPV wallet. 

12.	Ulordrig 
Ulordrig is a high-performance CPU version of the ulord mining program, forked from xmrig (https://github.com/xmrig/xmrig). Ulord provides a proof of work (POW) algorithm that can work efficiently on CPU but is difficult to implement efficiently on GPU, FPGA, and ASIC. Currently, it officially supports Windows and Ubuntu.

13.	bitcore-node-ulord 
A Ulord full node for building applications and services with Node.js. A node is extensible and can be configured to run additional services. At the minimum a node has an interface to Ulord Core v0.12.1.x for more advanced address queries. Additional services can be enabled to make a node more useful such as exposing new APIs, running a block explorer and wallet service.

14.	py-ulord-api 
A python version SDK that uses the ulord platform, which includes creating user relational databases, resource databases, and related queries. It encapsulates the ulord platform's http calls to facilitate the rapid creation of ulord applications.

15.	ulord-blog-demo 
   A blog system demo of ulord open platform based on nodejs middle layer, express framework and paython background. The main part is divided into the front desk including the user registration login panel, the article content list, and the pagination; the content details page including the article content display, the article payment view, and the article release page, etc.

16.	ulord-node-stratum-pool 
   This is a Cryptohello mining pool based on the Node Open Mining Portal project. The project is based on nodejs v4.8.7, requires support for rdis v2.6, and daemons. Here is the step for using mining pool: (1) Download and install dependencies. (2) Configure your pool_config directory, create an ulord.json and customize your own configuration against the example file. (3) Start the mining pool. 

17.	node-stratum-pool
High-performance mining pool service based on Nodejs. An instance can manage mining pools of multiple coins, and each type of coin can configure their own daemons and interfaces. This module cannot work alone, and is just used with Ulord (Node Open Mining Portal) processing mining certification, as well as raw shares data processing.

18.	Uschema 
Uschema is a protobuf schema that defines how claims are structured and validated in the Ulord blockchain. There is also code to construct, parse. It is used to define the format of the data and validate it in the Ulord blockchain.

19.	bitcore-node-ulord 
   A Ulord full node for building applications and services with Node.js. A node is extensible and can be configured to run additional services. At the minimum a node has an interface to Ulord Core v0.12.1.x for more advanced address queries. Additional services can be enabled to make a node more useful such as exposing new APIs, running a block explorer and wallet service.

20.	Ulord –platform
Ulord platform is decenterlize content distribution platform which can supply content repo, distribution and search ability, makes enterprise development content distribution more effective. Ulord platform software enables developers to create and deploy high-performance, horizontally scalable, blockchain infrastructure. This code is currently alpha-quality and under rapid development.

21.	bitcore-lib-ulord
A pure and powerful JavaScript Ulord library. Its principles: Ulord is a powerful new peer-to-peer platform for the next generation of financial technology. The decentralized nature of the Ulord network allows for highly resilient ulord infrastructure, and the developer community needs reliable, open-source tools to implement ulord apps and services.

22.	insight-api-ulord
A Ulord blockchain REST and web socket API service for Bitcore Node Ulord. This is a backend-only service. If you're looking for the web frontend application, take a look at https://github.com/UlordChain/insight-ui-ulord.


23.	insight-ui-ulord
Ulord blockchain explorer web application service for Bitcore Node Ulord using Insight API Ulord. Please see the guide at https://bitcore.io/guides/full-node for information about getting a block explorer running. This is only the front-end component of the block explorer, and is packaged together with all of the necessary components in Bitcore.

24.	slips
SatoshiLabs projects need a way how to document their technical decisions and features. For some of them Bitcoin Improvement Proposal (BIP) is not a right place because their range and implications are outside of the scope of Bitcoin and cryptocurrencies. SLIP repository is an extension to Bitcoin Improvement Proposal (BIP) process and contains the documents that are unsuitable for submission to BIP repository.
