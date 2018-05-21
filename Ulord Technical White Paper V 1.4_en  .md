![ulord](https://github.com/UlordChain/Document/blob/master/Technicalwhitepapercover.png)

 
**5000 years ago, humans invented characters and started the journey of civilization, hence started distributing knowledge and information;**  
**1000 years ago, human invented printing, discovering the importance of knowledge distribution;**  
**For nearly half a century, human invented the computer and the Internet and initiated the information superhighway.
Today, we have Ulord, making knowledge distribution a reality...**  
### Ulord——initiated a new era of digital resource value communication!   
**We are committed to building a blockchain digital resource distribution platform that is open, equal and respects creation.**  


# Contents  
- [Abstract](#abstract)  
- [Preface](#preface)  
- [Design idea and innovation point](#design-idea-and-innovation-point)  
  - [Background](#background) 
  - [Design inspirations](#design-inspirations) 
  - [Innovation point](#innovation-point)  
  - [Developmental vision](#developmental-vision)  
- [Architecture of Ulord](#architecture-of-ulord)  
- [Ulord platform](#ulord-platform)  
  - [Ulord protocol](#ulord-protocol)  
  - [Ulord network service](#ulord-network-service)  
  - [AI service module](#ai-service-module)  
- [Ulord original chain](#ulord-original-chain)  
  - [Master node system](#master-node-system)  
  - [Voting system](#voting-system)  
  - [Budget system](#budget-system)  
  - [Smart contract](#smart-contract)  
  - [Consensus algorithm](#consensus-algorithm)  
- [Application design and framework implementation](#application-design-and-framework-implementation)  
  - [Main characteristics](#main-characteristics)  
  - [Distribution mechanism](#distribution-mechanism)  
  - [UlordToken allocation scheme](#ulordtoken-allocation-scheme)  
  - [How to get UlordToken](#how-to-get-ulordtoken)  
- [Ulord Team](#ulord-team)  
  - [Core Team](#core-team)  
  - [Advisers](#advisers)  
  - [Investment agency](#investment-agency)  
- [Project promotion plan](#project-promotion-plan)  
- [Summary](#summary)  
- [Disclaimer](#disclaimer)  
- [Version statement](#version-statement)  
- [Power of interpretation](#power-of-interpretation)  
- [References](#references)  


# Abstract  
With the further development of Internet technology, Internet and service develop toward the direction of high centralization, which brings bloated, inefficient and costly problem. The blockchain technology creates a new revolution in the Internet world, and decentralized and trusted technology replaces the traditional centralization role, so that the whole world is organized into large value communication Internet to achieve a rapid evolution from information Internet to the value Internet. In recent years, with the rising of value of digital virtual currency, the blockchain technology has the worldwide attention, but a large number of investors just consider the digital currency as the appreciation, hedging tool, ignoring the real value of blockchain. How to use the blockchain technology in reality application has become a great challenge in the world of Internet.  
The project focuses on master node system, voting mechanism, InterPlanetary Domain Name System, interstellar domain name system, sidechain technology, consensus mechanism, smart contract, machine learning algorithm, other key technologies of blockchain, and artificial intelligence, aiming to develop a public blockchain that can be applied to many applications. Based on the public blockchain, a complete set of agreements can be established and provide all kinds of friendly API to allow third-party developers to build their own applications on top of its open source agreement, which can be widely used in knowledge sharing, ad delivery, code sharing, live video and other fields. It changes and reshapes the current situation of the industry in these fields so that the centralized platform between the publisher and the consumer of information resources will no longer be the leader in the resource and value communication, and thus break the shackles of the Internet that can not effectively transmit the value. It makes the transfer of knowledge and information more smooth and extensive, and gradually establish a good ecology featuring basic public blockchain, chain applications, value creation, information consumption and the participation of many actors such as developers of open source communities.  

# Preface  
The birth of the blockchain reflects that the human starts building the Internet with real trust. The blockchain is essentially to record the distributed database of all transactions or digital events, can also be considered as a public ledger, and all the participants can visit and record it. The blockchain can build reliable trust between points in the Internet to eliminate the intermediary interference in the value delivery, so as to realize public information and privacy protection, both common decision and protection of individual rights and interests, the mechanism enhances the efficiency of value interaction and reduces the cost, and has wide application prospect. This disruptive technology contains a huge of opportunities, and this change is just prelude.  
Ulord focuses on creating a peer-to-peer value transfer public blockchain, allowing third-party developers to build their own applications over their open-source agreements, which means to create various scenarios based on the public blockchain, including text, images, music, video, software, etc. The third-party developers can issue tokens to build their own economy or bulid various applications mainly around Ulord, using UlordToken in Ulord as an in-system credential. For example, an experience sharing platform can be set up on Ulord. Experience sharers price the published experience. Those who acquire experience information trade on the platform, and each fee paid to the experience sharer will be credited instantly. Product promoters can advertise on Ulord, price their ads, and people who are interested in advertising and clicking on the ads can get certain benefit. The producers of 3D animations can build sites on Ulord, peddle their own animation material, and those who has direct need can directly pay for the material, etc. In the past mode of information delivery based on the platform or other centralized agencies to get profit, now the intermediate links are removed. The information provider and consumers directly dock on the Ulord platform to maximally ensure the interests of the original creators.  
In order to support building and operating of decentralization content distribution platform, according to the characteristics of its application, the Ulord platform integrates the bottom blockchain service and P2P distributed service together, providing the high-quality Internet content distribution service based on blockchain for the majority of users. Ulord is mainly composed of Ulord platform and Ulord original chain, in Ulord platform provides massive cloud storage space, data sharing service with high QoS (Quality of Service), convenient content distribution site deployment, and creates good user experience; the original chain of Ulord is introduced into the master node net to provide a stable net and storage infrastructure, and by voting and budget mechanism, it can ensure the ecological, healthy and orderly development of Ulord, and combined with smart contract, it can make the user to make convenient deployment of distributed application to achieve perfect supporting of the entire ecosystem.  
This white paper in detail describes the design concepts, functions, innovations, architecture, key technologies and application scenarios of the Ulord project.  

# Design idea and innovation point  

## Background
Science and technology are the locomotives of historical development, creating new social forms. The development of science and technology has promoted the changes in all the elements within the productive forces, and triggered the changes in industrial structure, economic forms, as well as the mode of economic growth so as to push the corresponding changes of social relations of production. From the perspective of historical development, the emergence of iron tools greatly enhanced people's ability and efficiency of working in arable land, and broke the situation of slave owners oppressing a large group of slaves to collective farming. The family-based model of farming emerged and the cultivated land was greatly expanded, which brought the feudal society's production relations; the first revolution in science and technology initiated the era of substituting manual labor for machinery. The industrial production required large-scale collaborative production. As a result, peasants migrated from home to work in factories and formed industrial relations in production. In the information age, the network allows people to have no physical distance restrictions, and data becomes an important means of production, which also brings about new production relations in the information age. People gradually accept the concept that data means wealth. But by the time of the Internet popularization, is it possible that the data of each one become wealth? Not necessarily so. Most of our data doesn't produce value, and some of it is even used by some platforms as an important source of wealth. The world needs change, and we want to put the right back into the hands of data creators, just as workers want to get back their own land on which they live. The rapid development of information technology is bound to give birth to the new relations in the information society.  
The very beginning of the Internet was advocated as a free and equal thought. But the data and the liquidity of the data create the gap between the ideal and the reality. In the data transaction and knowledge transfer process, many problems cannot be ignored:  

- **The confirmation of copyright is difficult, and information creators are hard to get a corresponding return.**  
With the further development of copyright economy in recent years, people's awareness of copyright has increased gradually. In fact, in addition to the traditional books, music, movies, copyrights, many personal creation or experience has copyright, but this kind of copyright is often difficult to confirm. Individuals tend to be rewarded by the flow or the influence, but it is difficult to make their own ideas or experience rewarded. And even if there is a way to confirm the copyright works, the centralized broadcasting organizations or platforms play a leading role, especially the Giants which have formed in some industries even as a decisive role in information dissemination. Creators must obey the rules which are established by the central organization if they need to get user approvals, and the transaction process is cumbersome and always controlled by platform. Therefore users are hard to get reasonable rights and interests, which seriously frustrates their enthusiasm and creativity to create high-quality contents.  

- **Digital content quality varies greatly; users cannot get good contents quickly**  
In the era of mobile Internet where the flow rate is considered as the most significant aspect, public attention becomes a new scarce resource. However, when there are a large number of headline parties and sensational information, users are hard to make effective screening when facing such a large amount of information in a short time, or even fulfilled by a lot of spams and advertising information which likely reflects a “lonely voices” in creating high quality contents, so as to threaten the living space of creators seriously. It is hard to balance the high-quality production and efficient dissemination of the content, ultimately resulting in “poor coins drives out good coins”. It is nonsense to improve the current situation by relying on a centralized platform. The economic base determines the superstructure, and only disruptive technologies and mechanisms can accomplish this revolution.  

- **Internet Information exploding, lower accurate matching rate between users and contents**  
Information platform attaches great importance to how to capture users and take a huge price in in advertising marketing, operations management, branding. But there is still a big gap in user habits, depth of interest mining, and the accuracy of information push. For example, in advertising delivery, people are passive to accept ads, and product promoters have to pay a large amount of fees to advertise media company, while the ads may not be able to accurately push to potential users. The so-called precision information delivery is to start from the user behavior to get potential customer information, this approach has a high threshold for the data, and ultimately only the "oligarchs" platform will have the opportunity to achieve through technology.  

**Faced with a huge market prospect, blockchain technology as an effective way to solve the plight of content distribution industry, has drew great attention between technology enthusiasts and investors who have sensitive olfactory.** At present, some projects are trying to make use of blockchain to make changes in the information and content industries, but all in an initial stage. There is no mature product or model can bring disruptive changes to the industry.  

## Design inspirations  
Blockchain is the underlying protocol of next-generation Internet, all applications built on which naturally have an almost independent economic system, and the rules of profit distribution in this economy can be clearly defined by smart contract.  
Ulord project is proposed and developed, which is mainly from the following three aspects:  

- Firstly, the characteristics of blockchain technology can effectively solve the problems of content distribution industry. The copyright confirmation and content distribution are united, and the content publishing mode of the current entertainment and publishing industry is changed and re-defined. After decentralization, only two of the most basic roles exist for the content distribution industry: the creator (Producer) and the user (User), in this case, efficient and reasonable distribution of interests will be made. There is an urgent need to solve the technical difficulties and the mechanism innovation in the content distribution.  

- Secondly, blockchain is at the primary stage of development, and there are a lot of public blockchains. Consequently a wide variety of applications appears, but the public blockchain to effectively support the content distribution has not yet appeared, which cannot bear rich website service type in content. Especially in data storage, data quality of service and content payment model, there are many problems. It needs blockchain platform to solve the pain points of content distribution industry;  

- Thirdly, from blockchain itself, the existing blockchain technology has many urgent problems and bottlenecks, such as internet congestion, delayed payment, obvious mining centralization trend, high resource consumption, and some public blockchains with security vulnerabilities, which is difficult to meet the practical application requirements. So there is an urgent need to take further research and practice to solve the above problems in the blockchain underlying technology, promoting the fast blockchain application and development.  

Ulord is a distributed P2P internet open source project based on blockchain technology. Different from our daily access to the internet server, there is no concept of server in Ulord, all internet data are scattered in various Ulord user's computers, and people only need a pair of asymmetric key to publish their own site. Everyone can find the site service announced by the publisher through the search and domain name, and directly download the site data in P2P net. After more and more people’s visit, the publisher's site will be stored by many computers. Those computers with access to your website will start to make the seed for your site, just like the BT seed, and the content of your site will continue to exist in numerous computers. In Ulord, in order to provide a better user experience, two kinds of role node are used for storage of data, and one is the master node role. The user of this role stores the data on Ulord through providing storage service with high QoS, at the same time, earns the income according to the provided storage space; the other is the common user computer role, which can only backup the user's favorite resources as a supplement to the master node role. When the users get access to the site service, through the distributed hash table (DHT, Distributed Hash Table) technology, it allows users to quickly download the required data segment from the P2P net, and then it is assembled by the client to restore the complete data. Due to the technology of P2P for bearing, Ulord resources have high availability without downtime.  

## Innovation point  
From design, we will isolate the system into two levels, the bottom “operating system” and the upper layer “application program”. The infrastructure of transparent and open ledger and smart contract that cannot be tampered is established at the bottom, and the upper application program is used for completing the business logic without considering how to develop the decentralization application.  
For the original chain of supporting content publishing platform is concerned, we will carry out some original work based on this application scenario, including:  

- **The master node system is introduced to solve the problem of long communication delay, and small storage space etc.**  
The new mechanism is designed to encourage users and investors to participate in the master node Ulord construction, and provide stable QoS data storage service; it provides a variety of cross-platform solutions, which is convenient for the users to master node deployment service, including Linux/Windows/OSX and other mainstream operating systems; through the master node service, it can support more than 4000 of the trading frequency per second to better meet the practical application.  

- **The voting mechanism is established to promote community development and content review**  
It allows each user on the Ulord to vote for the Ulord resources, the site and the suggestions for the improvement to achieve two goals: one is to assess the plan proposed by the developers to promote the community contribution to Ulord; the two is to review the resources and sites on Ulord to maintain ecological, healthy and orderly development of Ulord.  

- **Reasonable income distribution mechanism is set to stimulate the majority of developers to contribute**  
10% of revenue is set aside to the entire community's developers, and fund the developers to perform meaningful development plan. The evaluation mechanism of code review and task quality evaluation are introduced to supervise the funded projects to be completed as required on time, form a virtuous circle, and promote the ecological and healthy development of Ulord.  

- **InterPlanetary Domain Name System is established to provide a unique, simple and readable domain name service**  
The blockchain resources are usually represented with the address of 34 character strings in length, which is not easy to remember, nor convenient to use. In Ulord design, through the establishment of the InterPlanetary Domain Name System (IPDNS), it provides decentralized domain name analysis service for the users. Example: Ulord user releases resources, and there is no domain name resolution, through https://ulord.one /U45c21eP5QGefi2DMPTfTL5SLmv7DivfNa access. After he applies for a domain name service, he can directly access it through uld://ulord.one/Alice, where Ulord is the requested custom domain name, and U45c21eP5QGefi2DMPTfTL5SLmv7DivfNa is the resource address.  

- **The sidechain technology is introduced to achieve rapid deployment of smart contract**  
The sidechain technology can be used to achieve being compatible with Ethernet virtual machine, and release of smart contract. Any user building the site in Ulord through the friendly API, providing Internet content distribution service, can customize their tokens, and operate their own site by tokens. Tokens can be converted to a certain proportion with UlordToken.  

- **The mixed consensus mechanism of PoW + PoS is used to attract more idle resources to join Ulord**  
In order to better load application on the Ulord platform, the design implements a hybrid consensus mechanism: PoW (Proof of Work) and PoS (Proof of Storage).PoW algorithm is used for accounting with a new CPU mining algorithm CryptoHello which can effectively resist all kinds of known and unknown attack through the AES algorithm and the improved algorithm; PoS algorithm is suitable for the construction of IPFS infrastructure, and encourages more users to provide large storage space for storage of data on the Ulord platform.  
The main innovations of the Ulord's platform layer and application layer include:  

- **A distributed file storage, retrieval and distribution mechanism based on blockchain are designed and implemented**  
Based on the bottom blockchain, integrate the P2P downloading, distributed file organization and intelligent learning module, provide quick content search service, content distributed storage service, customized service of node, peer-to-peer content distribution service, distributed hash indexing service and cyber source self-purification service.  

- **An efficient communication model of value**  
It establishes the value transmission chain of content distribution process, encourages users to participate actively through profit distribution mechanism, so that the users are willing to contribute valuable contents and efficiently perform excellent content dissemination.  

- **It supports intelligent push of contents based on the AI algorithm**  
a) According to the data of high dimension, mixed type and strong timeliness, a multi-source knowledge extraction and association method based on deep neural net is designed, which realizes entity name recognition, entity attribute extraction method for the site, content and author and other essential information;  
b) Through the hybrid model method, collaborative recommendation method based on knowledge embedding and recommended method based on online real-time feedback, we achieve intelligent push of content for different users and different dimensions;  
c) Through hybrid recommended method based on domain knowledge, and with the integrated knowledge structure feature, topic feature and semantic features of content vector space modeling technology, the mixed recommendation of the recommended method based on content and collaborative recommendation method can be achieved.  

- **Content control and promotion of communication based on AI algorithm**  
a) Through the integrated knowledge structure feature, topic feature and semantic features of content vector space modeling technology, the sensitive information can be examined automatically.  
b) The communication path based on the knowledge map is selected and optimized; through the recombination of related contents, content access and the user experience are improved.  

The innovative design of these technological routes and ecosystems provides strong support for Ulord, and tries to innovate the current status of content distribution industry and promote its healthy development.  

## Developmental vision  
Ulord aims to reconstruct the benefit distribution of information delivery through a decentralized approach, to make all data and knowledge valuable, so that all the values are returned to creators. It makes information autonomy, the benefit right decided by the information producers, and reduces the intermediate control of information and value conversion.  
Ulord is a sword to transform the Internet world through blockchain technology.  

- **Payment for contents in new system - effective transfer of value**  
In decentralized system, content only includes the charging and payment, the former is to be paid, such as novel, music, film and television, and the latter is paying for others to see, such as advertising. Both in charging and payment, the content publisher will directly transfer the value effectively without intermediate link for bargaining or consumption of resources. If the traditional centralized platform loses its bargaining power, is there no incentive to participate in new system? In fact, they still have more motivation to join. For many not-so-famous creators, they work with the platform partners and give up some of the benefits to quickly make their works in the market. As for the best content, authors and platforms can gain greater value.  

- **User behavior in the new system and content distribution mechanism innovation**  
Processing of contents by user is divided into stop and promotion of spreading. Negative comment means stop of spreading, positive comment means promotion of spreading, and forwarding content is the new content distribution mechanism. The decentralized net can use consensus mechanism to make scoring for the user with behavior to find the real user with the ability to identify and hatch the contents. Once user forwards it, the user is equivalent to play the distribution ability, and should receive rewards of content. The more rounds of forwarding lead the more corresponding return. In fact, through contract mechanism, the users in the process of transmitting contents is to buy the copyright of original author.  

- **Content industrial revolution - good coin eliminates poor coin**  
It says no to the mixed information, and filters out the value through technology and mechanism. Valuable information can stand out and worthless information is eliminated by the mechanism. For example, in publishing industry, the last two acts of production, issue, and distribution (issue and distribution) are all done by users, and new distribution of benefits also gives them enough incentive to do better. As a result, content production will be more sophisticated and outstanding creators more indignant - as long as you are certain that what you make is the real need of the world. There's no need to be afraid of not being recognized. We are determined to rely on the blockchain technology to establish a new Internet order.  

- **Decentralized new world - ecological circle and incubator**  
No application can meet all needs, so you can develop a variety of applications in Ulord, which is more like a blockchain application incubator. On this base, we will develop and invest a lot of specific applications. The first Ulord application will be developed by us as an example, which is a strong relationship based information publishing system. Smart contract is added on the base for the benefit redistribution to make content producers and distributors get payback. Barrier of traditional platform access to blockchain will be continuously lowered, and users do not need to have insight into the technology of chain and can publish their applications by friendly API.  
In short, Ulord is determined to use blockchain technology to create a new generation of digital resource interaction platform, which aims to create a basic public blockchain. Ulord adheres to the idea of freedom, openness, respecting for creation and faces the global ecosystem, with the advantages of affirming and distributing copyright, no platform fees, integrated payment system, supporting different digital content formats and more convenient transactions.  

# Architecture of Ulord  
The modular design of loose coupling is adopted for Ulord in overall design, which encourages more developers to join in the development of the entire ecosystem. Through web interface, desktop application and mobile APP and other forms of display, the application layer publisher can more easily build site, and publish Internet content distribution service of his own. Architecture of Ulord is as shown in Figure 1, which is composed of Ulord platform and Ulord original chain. Ulord is the P2P data service, including data transmission, data distribution, data storage, data index, accounting model, communication model, Gas model and payment system. The original chain of Ulord is blockchain infrastructure, providing accounting, domain name, master node and other services, so as to ensure that the entire backbone of network is stable and orderly.  

![Architecture of Ulord](https://github.com/UlordChain/Document/blob/master/Figure%201.png)

# Ulord platform  
The platform layer is the middle layer of the system, and plays a role as a bridge between application layer and base layer. The platform layer is categorized as support component and function component according to function. The support component provides functional components with basic function supporting. The platform layer is connected to blockchain of base layer through the functional components, providing the application layer with content distribution, sharing and payment service based on blockchain. The platform layer architecture is shown in Figure 2.  

![Ulord platform](https://github.com/UlordChain/Document/blob/master/Figure%202.png)

The core function of the platform layer is to build a basic network and service environment for content sharing platform. The main functional modules are as follows.  

## Ulord protocol  
Ulord protocol is foundation of data transmission and service layer. The user based on Ulord protocol can upload resources quickly, search and purchase the interesting content. Ulord protocol realizes data distributed organization and accounting by defining a series of rules.  

- **Distributed general ledger**  
The foundation of Ulord protocol is distributed general ledger, which is the foundation to generate encryption currency (UlordToken). The difference between Ulord system and traditional bank and payment system is the trust system based on decentralization. The trust mechanism is achieved through interaction of different participants. Through a distributed consensus mechanism, the transaction becomes credible and every accepted transaction will be recorded in blockchain, namely distributed ledger establishment.  
Storage of internal data of Ulord blockchain is carried out in the key value pair. Each key corresponds to corresponding resource or its metadata name, and through the search based on key name, the content resources of user's attention is returned. In addition to name and element of the stored resources in Ulord, the remaining data storage mode of blockchain is completely consistent with bitcoin block structure. But the block hash algorithm, block reward function, block size, total number of blocks and offline chain in this project are optimized. 

- **Ulord network**  
Ulord network is the infrastructure to extend Ulord blockchain original accounting and payment function. Its main function is to provide the internet environment for the users in paying, searching, downloading and uploading resources in blockchain. Accessing to Ulord is a prerequisite for sharing and distribution of contents. Different from HTTP, DNS or other protocols of traditional www Internet, Ulord network is based on Ulord protocol for user communication and data exchange. In application form, Ulord acts as the background daemon. On the one hand, it monitors the data request of the machine; on the other hand, it monitors other nodes in the network and exchanges data with them.  

## Ulord network service  
Ulord network service is based on Ulord protocol, integrated with P2P downloading, distributed file organization, intelligent learning and other technologies, which constitute different functional modules. Ulord network service can be flexibly set according to user's needs. Currently, the services provided mainly include the following categories.  

- **Fast content search service**  
Ulord protocol provides metadata-based resource classification function. Each user resource can not only follow traditional search function based on description information, but also has the following characteristics: a. It provides fast resource location based on content addressing, rather than based on domain name addressing. File has a unique existence. When a file is added to Ulord network, a unique encrypted hash value will be assigned to the content based on the calculation. b. In addition to storage of hash value, blockchain running on Ulord is extended to support the storage of hash value table of files. When each network access occurs, query of the address of the file on chain is conducted.  

- **Content distributed storage service**  
Ulord uses P2P hypermedia protocol, making the internet faster, more secure and more open. All nodes in Ulord form a globally oriented, peer-to-peer distributed file system, and all computing devices with the same file system are connected together. Each file and all the blocks are endowed with a unique fingerprint called encryption hash. Each node, through determining of hash value of file, judges the redundant files, to ensure that the data is not redundant in a single node. In the search for documents, you can find file storage node by the hash value of file to find the file you need; next, Ulord provides the history version controller of file, supports multi-node using and saves different versions of files to achieve file's history status tracking.  
Secondly, file storage in Ulord is not mandatory for every node to store all  contents. The owner of node can choose data to be stored. For the nodes stored with large amounts of content, Ulord billing model automatically calculates the user benefits through the data amount of downloading service of file, so as to encourage users to upgrade their hardware resources to provide more comprehensive data storage and maintenance service to obtain benefits.  

- **Node customization service**  
Ulord node includes centralization node and lightweight node. The centralization node has client to store all historical records (all transactions of all users) of UlordToken, manages user's wallet, and can directly start trading on Ulord network. Node can handle all aspects of agreement, achieve independent verification of the entire blockchain and any transaction, and provide completely autonomous and independent transaction verification. But the centralization node client needs to consume a lot of computer resources (for example, more than 125 GB disk, 2 GB RAM). The lightweight node is deployed with lightweight client. Lightweight client, known as simple payment verification (SPV) client, connected to the complete node of Ulord, and used to access the transaction information. But the local place is used for storing the user wallet, and is independently created, validating and transferring the transactions. The lightweight client and Ulord are directly mutual without intermediary.  

- **BitTorrent peer-to-peer content distribution service**  
Ulord, based on blockchain accounting, integrates BitTorrent peer-to-peer content distribution protocol, and adopts efficient software distribution system and peer-to-peer technology for sharing of large volume of files (such as a movie or TV show). Each of users can provide uploading service just like Ulord redistribution of nodes. In the traditional internet, downloading server provides each user issuing the request of downloading with downloading service. The working mode of BitTorrent is different. Holder of distributor or file sends the file to each user, and then it is forwarded by the user to other users; users forward their own files, until downloading of all users is complete. This method can make downloading server handle multiple files of large volume at the same time without occupying a lot of bandwidth.  

- **Distributed hash index service**  
Ulord uses a distributed hash table (DHT, Distributed Hash Table) to organize the namespace of the user resource. Through the DHT, the relationship mapping (key, value) is realized in network nodes. DHT is a distributed system without center point to provide the key->value query. The mapping information from key to value is stored in many nodes in a distributed manner. Changes of data and node will only affect part of nodes, without an impact on all nodes. As a basic architecture, DHT can be used to build more complex applications, such as distributed file system, domain name service, instant messaging, P2P file sharing and content distribution platform. DHT defines a keyword space, such as bit string set of all 160 digits, then through certain algorithm, the keyword is mapped to all nodes of the whole DHT system. This algorithm is called consistent hashing. Through this algorithm, DHT can find a node according to a keyword and then operate the node, such as storing of data, query of data and so on.  
Each node in DHT only needs to be connected with other nodes. A keyword is used to access any node, and the node can transmit information to the node corresponding to the key for processing. This process is called key-based routing. The search engine can get seed file from DHT net node through the character string without relying on seed server. BT download uses the public DHT network, which can greatly reduce the dependence on seed server.  

- **Ulord resource self-purification service**  
Ulord is a decentralized network without center administrator to review and control content, so it is inevitable that there will be “inappropriate” content resources. Ulord is designed with network voting mode to support user node to initiate proposal, and vote on the content in the net resources. When voting results satisfy certain conditions, it is recognized as “inappropriate” content; the system can make “inappropriate” resources not be accessed by the unlimited increasing of resource charge or making resource offline.  

- **Billing service**  
In Ulord, communication, storage, release and downloading of resources, in addition to the completion of corresponding application functions, are regarded as a transaction in blockchain. Most transactions in the network contains transaction fees (miner fee), such as publishing and downloading of resource. In Ulord network, users are encouraged to publish and spread high-quality resources. The main billing behavior mainly includes the following categories  
  - Release resources: when users name the resources, it is required to deposit certain amount of UlordToken; the deposited UlordToken are locked in user account, which cannot be transacted. After the resources are withdrawn, the UlordToken will be returned to the user account after deducting transaction fee. Therefore, Ulord can effectively prevent resources from being maliciously released (Spam);  
  - Download resources: when users take online browsing, and download resources, the corresponding UlordToken in accordance with the set value of resources will be paid;  
  - Resources propagation: when users share resources of other users; when the resource is connected with consumption behavior, benefit from resources spreading can be obtained.  
  - Obtain benefits by providing resources storage: when user upgrades hardware, provide storage and download service as the central node, obtain benefits.  
  - Obtain benefits by providing computing resources: when user node participates in the distributed accounting as miner to obtain benefits from it;  
  - Initiate the proposal: when user initiates the proposal according to network content review, there is a need to pay UlordToken;  
  - System R&D/maintenance: the system will reserve a certain proportion of UlordToken for proposal voting, functional research and development.  

- **Integrated service process**  
The main process of platform layer service is as follows:  
  - User joins Ulord network, and searches a file called “XX comedy film” in the network through the client;  
  - Ulord network quickly index hash value on blockchain, and provides the relevant search results;  
  - The user pays the corresponding UlordToken according to the paying information of the returned file, and “XX comedy film” file is cached to local place. “XX comedy film” file is not downloaded from cloud or server, but certain one or some nodes in Ulord;  
  - In Ulord network, user resources are generally stored in Ulord nodes after being encrypted in blocks, and each block is stored in multiple user nodes or center nodes. Ulord network automatically searches the fastest way to download and recombine resources, so as to ensure that users can download file in the most efficient way;  
  - After the user caches the files on his computer, he cannot only watch it, but also share to others;  
  - You can also forward the resources in the network, and have the opportunity to get UlordToken.  

## AI service module  
In platform layer, we add AI service mode, and the data the mode needs to process comes from two ways: The operation data produced by the application layer, including user behavior data and application behavior data, etc. The operation data of the platform layer and the base layer. Through AI technology, the operation of the underlying system can be more secure, stable and efficient.  
The functions supported by AI include three parts: generation management, quality control and distribution effect management.  

**a. Generation management**  
It includes real-time tracking of popular sites and hot content, fast analysis of real-time, authority, influence and attractiveness of contents, information management and behavior analysis of high-quality authors. It attracts excellent content creators to build site by various ways.  

**b. Quality control**  
Original content validation: with block record information of the base layer, the originality of contents is analyzed, so as to prevent malicious imitation, and talking about old topics.  
Sensitive information review: in addition to voting review mechanism, the system takes the vulgar content recognition based on AI; through semantic analysis and image detection identification, it controls pornographic and political sensitive topics.  

**c. Distribution effect management**  
Accurate recommendation: the site's personalized content accurate push is achieved by searching users' concerns and interests through their visits (browsing page, browsing order, browsing time).  
The optimization of transmission path: based on the knowledge map, the propagation path is selected and optimized, the content access through the combination of the related contents is improved, and the user experience is better.  
Malicious node analysis: the malicious nodes of “strip wool” in the content communication link are identified and removed to safeguard legitimate rights and interests of real users.  

# Ulord original chain  
In order to meet needs of Internet content distribution, the original chain of Ulord introduces master node system. The structure of master node is established as a peer-to-peer distributed content distribution network (InterPlanetary File System, IPFS), which provides massive cloud storage resource pool and unified global addressable space storage resource. Considering the sustainable development of Ulord, voting system and budget system are introduced. Voting system can not only carry out intelligent evaluation on a variety of applications on application layer, but also can assist budget system, fund more developers to devote themselves into Ulord development, and make the ecological development of Ulord in a virtuous circle with more applications. In other implementations, Ulord can be compatible with smart contract, make the application of Ethernet be transplanted to the Ulord network. Ulord adopts the mixed mining mechanism of POW and POS, so as to ensure that the development of the block network is not held by hashrate.  

## Master node system  
The whole node refers to server or common PC running the full client on the P2P network, which plays a role of spread of transactions and blocks in the blockchain network. To maintain normal operation of all nodes, a large amount of cyber source needs to be consumed, such as storage space and network flow. According to Zap Chain Magazine statistics, the number of all nodes in the bitcoin network shows a decreasing trend, which requires additional 40 seconds for block broadcasting. The community has put forward many solutions, such as the introduction of new award plan of Microsoft Research and the Bitnodes incentive plan, and try to increase the number of nodes, but without good solution.  
![Master node system](https://github.com/UlordChain/Document/blob/master/Figure%203.png)

In order to maintain a healthy and stable blockchain backbone network, Dashi puts forward the solution of hierarchical network. Through the introduction of master node system, the stable backbone network can form to solve communication delay. In the system of Dashi, 1000 nodes of dash can be stored and upgraded to the master node. If it can be stable online in a period of time, 45% of income of each block network will be taken. But now, the master node system of Dashi still has many problems in the design and implementation. Firstly, according to the design rules of Dashi, the total number of coin of the whole system is about 17 million, and approximately 8 million have been issued. While the number of the master node is maintained at about 4800. As each master node needs to have 1000 dashes as guarantee, nearly 5 million Dashi coins are locked in master node. The number of circulating Dashi coins in the market is less than 3 million, which is obviously contrary to the initial design theory of bitcoin, and cannot guarantee a sufficient currency circulation in the market. Secondly, in the design of master node, there is no discrimination or considering QoS, and master node service quality is uneven. Therefore the network communication cannot achieve the desired results. Finally, only users with some computer knowledge can build master node, not all people have such a foundation. To entrust the third party often brings the risk to assets, so it is necessary to let more people participate in the maintenance of the master node network. As shown in Figure 3, considering different application scenarios, Ulord makes further improvement and optimization to the master node system as follows:  

**Voting mechanism of master node is introduced to enhance Ulord service quality.** In order to encourage users to join in the master node construction, Ulord distributes 25% of the entire network benefits to master node holders. While QoS assessment mechanism is introduced, and under the principle of survival of the fittest, some master nodes which do not meet the requirements will be eliminated. Therefore master node users must continuously invest and maintain to ensure good condition of nodes. QoS assessment mechanism mainly considers from the following several aspects:  

- Data packet loss rate: packet loss rate between master node and adjacent nodes is judged by ping-pong operation. If it exceeds a certain threshold, the node state is judged not to meet the service requirements, and the master nodes list is eliminated.  
- Network communication delay: the delay between master node and adjacent nodes is judged by ping-pong operation. If it exceeds a certain threshold, the node states is judged to not meet the service requirements, and the master nodes list is eliminated.  
- Data retransmission number: when retransmission times of master node and adjacent user node are too high, the user node will broadcast it on the entire network. When the reported number of this master node reaches the threshold, the master nodes is eliminated from master node list.  

**Proof-of-Stake mechanism is introduced to provide IPFS service.** In order to meet distribution mechanism of Ulord network, a large number of nodes are needed to bear the Internet data, and provide more high-quality video and data flow service. In Ulord, it ensures the network storage service with high quality from two aspects. First, in the Ulord network, 1TB of hard drive storage space is needed as a qualification guarantee for master node; through distributed technology, Ulord can integrate these master nodes into a massive storage resource pool. Second, in order to confirm that each master node is actually stored with data, Proof-of-Stake mechanism is introduced. This mechanism can randomly carry out integrity verification to the master node data by data holding proving and data recovery proving to ensure that the master node can provide stable data storage service. The main factors of the nodes are as follows:  
- Storage capacity: according to storage capacity size, the income is calculated in proportion.  
- Storage value: according to storage data value, determine whether the platform effective data are stored, and determine whether to calculate the income;  
- Store IOPS: IOPS (Input/ Output Operations per Second), that is the number of read/write (I/O) operations per second, measures the performance of disk random access. According to disk performance, judge whether to calculate the income.  

**More general master node platform.** Ulord will provide a better user experience for user, while bringing more high-quality storage and network server for the system itself. To attract more investors to participate in the construction of the master node network, we will develop master node client software across the platform, including windows/Linux/OS x/Android and other mainstream systems. For Linux system, Docker package image will be provided directly for users to install conveniently.  

## Voting system  
Voting system has two major roles on Ulord. The first is to evaluate the plan proposed by developers and promote community contribution to Ulord; the second is to review resources and sites on Ulord to maintain the orderly development of Ulord ecology. If there are developers contributing to Ulord good solutions or codes, they can get system rewards. Whether to award and how much reward of developers contribution are decided by community vote. In addition, Ulord allows users to publish their own site, which may cause the problem that a large number of applications launch make the entire ecosystem in disorder and difficult to govern. In order to purify the network environment and make Ulord ecology a healthy development, consensus evaluation mechanism is introduced for Ulord network intelligent maintenance. The resources posted by user on Ulord have a unique 160bit hash value. All master nodes can vote the site resources issued by users on Ulord and show their position. When the number of opposing votes in a certain period of time exceeds threshold value, the network will automatically prohibit resource transmission, and give time to make publishers rectify. If there is no rectification in the specified time, Ulord will automatically delete it. There are three kinds of voting types: yes, no and abstain.  

## Budget system  
In order to promote the healthy development of Ulord ecosystem, Ulord prepares 10% of income for developers of the whole community. Ulord provides unified proposal entrance for community development. The community developers can submit the improvement proposal of Ulord through the entrance. The submitted proposal will be broadcast to Ulord, and sent to users in the form of message. All Ulord users have rights to vote. When the number of a proposal support exceeds a certain threshold value (the current system is set to 30%), the proposal will be approved. Then, the developer submitting the proposal will begin to accept budget system support. For the same proposal, users need to make voting twice. After the first voting, development team will receive budget support, but only 50% of the budget will be provided for developers. Only after developers complete and launch the second voting, the user can receive the remaining 50% of budget support.  
In concrete implementation, a super block will be automatically generated in every 17000 blocks, and funding for the community developers can be achieved through this block. The number of coinbase coin of super block is the sum of the blocks between the previous super block and the current super block after deducting of 10% of income, then txout is the budget address passing the budget. If the current super block has no budget, the funds will be automatically stored in the pool of funds, which is used for the following plan budget support.  

![figure4](https://github.com/UlordChain/Document/raw/master/img/figure4.png?raw=true)

## Smart contract  
### Unified domain name mechanism  
Ulord allows the users to call the API of platform layer to publish their own site service. In order to make Ulord users to get convenient access to other users' resources on the Ulord platform, the readable character string easy to remember can be used as domain name. Before the user releases the resource, by specifying the domain name site, he can apply for the readable domain name easy to remember. But there is a need to bind certain amount of UlordTokens. With the passage of time, the quantity of UlordTokens will be gradually consumed with increasing of block; in other words, all the resources and websites on Ulord will be gradually consumed with the increasing block height. All UlordTokens consumed for applying for a domain name will flow into the underlying network and become a part of the cost of billing.  
To support the readable domain name system, we introduce a new data structure Domain Claimtrie to store all domain names and the associated information on Ulord. As shown in Figure 5, in Domain Claimtrie, each node corresponds to a domain name, at the same time, each node also holds the node's related transaction information, including a transaction. When the user applies for the domain name, it must be bound with a certain number of UlordTokens; the new domain name is allowed for registration, which is unique in Ulord. The user is supported for cancellation of domain name. After the domain name is cancelled, the domain name is automatically released. To support the integrity of the domain name tree, we modify the block structure of blockchain and adds a field Domain Claimtrie.  

![figure6](https://github.com/UlordChain/Document/blob/master/Figure%206%2B7.png)

### Properties of smart contract  
Ulord has attribute of smart contract, and introduces the design concept of gas. But Ethernet gas consumes gas in each operation. Compared to the gas concept of Ethernet, Ulord adopts a more simplified and abstract method. The resources and site posted on Ulord by user will consume resources on the Ulord network. Therefore when the user releases resources or site, a certain amount of UlordTokens is needed to bound. With growing of block height, UlordToken will be gradually consumed, and the user needs to recharge the new UlordTokens to the corresponding address to ensure the ownership of domain name. At the same time, through sidechain technology, it can be compatible with Ethernet virtual machine, release smart contract, and allow users to publish their tokens. There is a certain proportion of exchange relationship between tokens and UlordToken. Ulord allows users to customize their releasing of site service, and through the issuance of their tokens, they can operate their own sites.  

## Consensus algorithm  
Ulord combines PoW (Proof of Work) and PoS (Proof of Storage) as the consensus algorithm. Among them, PoW uses the self-designed CryptoHello algorithm. The algorithm uses multiple serial cryptographic primitive operation. With the characteristics of computer architecture, it has the mining characteristics of permanent prevention of ASIC. POS mechanism is to encourage more master nodes to join. By providing more storage space, it brings in revenue for their own, and provides massive distributed storage space for Ulord.  
###	PoW implementation mechanism  
In order to make full use of idle resources for mining, the original chain of Ulord adopts the self-designed CPU algorithm of mining - CryptoHello algorithm. The algorithm is proved to be secure in random model. CryptoHello algorithm is as shown in figure7.  
![figure7](https://github.com/UlordChain/Document/raw/master/img/figure7.1.png?raw=true)

The input of the algorithm is the Hash value of the last block Mi-1，the block head data TD and Nonce value. Firstly, through a fixed filling algorith, length of Mi-1||TD is integer length of 1600bit. Then the filled messages are grouped according to 1600bit, and they are recorded as N0,N1...,Nt-1, C0=Nonce.  

First step: iterative computation Cj = f(Cj-1 *xor* Nj-1), in which,j=1,...,t, f is internal permutation of 1600 bit Keccak algorithm, state value of 1600bit Ct is obtained.  
Second step：prepare 656 copies of Ct, and it is divided into  T0,...,T8199 according to 128bit, the sub-item is recorded as Q0 = AES(T0), then iterative calculation Qj = AES(Tj *xor* Qj-1)  is carried out, the key value is:  
K=0x123456789abcdef0123456789abcdef0.  
Third step: calculate , then iterative calculation  
Rj = AES(Rj+1 *xor* Qj)is carried out.  
In which,  *xor* is the multiplicative operation on a finite field, and aes is AES algorithm of six rounds, and the key is same as above.  
Fourth step: SHA3 algorithm is used to calculate the hash value of R0||R1||R2||R3, and the lowest 256 bits are output.  

Safety note: Sponge structure is the current main structure to design the password algorithm, so the CryptoHello algorithm uses the Sponge structure. As the winning algorithm of American SHA3 plan, the security of Keccak algorithm has been widely studied and approved in the cryptography community. Meanwhile, whether it is hardware or software realization, the Keccak algorithm has certain advantages. At present, the preimage attack to SHA3 algorithm is not more than 7 rounds, and not more than 5 rounds can be transformed into real attack, because the Keccak algorithm actually has 24 rounds, and Keccak algorithm can resist preimage attack.  
AES algorithm is the most widely used grouping cipher algorithm with high security at present. The actual number of the rounds can be broken is 5 rounds, and CryptoHello algorithm uses complete ten rounds of AES algorithm to extend the message length. The simplified AES algorithm is used to achieve the message compression; the multiplication over finite field can effectively resist the spread of high-probability difference. So AES algorithm and its deformed algorithm can effectively resist all kinds of known and unknown attack. The final data processing is processed by SHA3 with high safety.  

### PoS implementation mechanism  
The main reason for collapse of bitcoin network node is lack of reward for  running nodes. With the passage of time, more and more users will be connected to the whole network, so demand for bandwidth will become higher, demand for funds from node operator will be more, then the operation cost of the nodes increase. Considering rising cost, node operator must reduce their operating costs or operation light client, but this is not conducive to network health. The introduction of the master node technology can effectively avoid reduction of master node and prolong communication time. In Ulord, QoS is considered in the selection of master node, and master node is a full node. Block and trading can spread quickly through master node. Operation of a master node needs 10000 UlordTokens and more than 1TB of storage space. The deposit stored in the master node is not lost, which allows investor to earn certain return on investment when providing service for the whole net to reduce the UlordToken price volatility. In the Ulord network, the master node will account for 25% of the entire network revenue.  

## Others
### Privacy protection  
Ulord uses the most popular privacy protection zk-SNARK technology to protect the trading privacy. In Ulord blockchain, to create a valid transaction includes the following three things:  
- a. Ensure that the currency in the address has not been spent in previous trading;  
- b. The sender proves that he is the currency “holder” in the way of authorized signature;  
- c. The transaction input is equal to output.  
The ledger itself proves the money is not spent out before and does not require sender to do anything. The sender only proves that he is holder of the currency, and hopes to send out the currency in the way of electronic signature through the private key corresponding to address. To make the signature verified, the sender's address must be open. Correspondingly, receiver must publicly accept his address to finish the transaction. In Ulord, it is simple to verify that the input and output of the transaction are equal, because the number of transmission is completely exposed.  

![figure8](https://github.com/UlordChain/Document/raw/master/img/figure8.png?raw=true)

Zero knowledge proof (specifically, zk-SNARKs) to verify the above three elements can protect privacy of users from revealing, without exposing sender, receiver and transferring amount. Every successful transaction is accompanied with zk-SNARK, and it proves that: the input asset exists, and has not been previously spent. The person who creates the transaction authorizes the transaction cost, and the input number and type are equal to the output number and type. The information for cost output (that is to create a new zk-SNARK) is attached to the transaction. It is encrypted with the public key of payee, and only used for the payee.  

![figure9](https://github.com/UlordChain/Document/raw/master/img/figure9.png?raw=true)

### Instant payment  
With the master node technology, the users can send and receive instant irreversible transaction. Once the instant transaction forms, the input of transaction is locked to the corresponding particular transaction, currently, the locking time of the whole net transaction is about 4 seconds. If a locking consensus is reached in the master node network, all transactions and blocks against it will always be refused, unless they can match the corresponding transaction ID which was locked at that time.  
In this way, users can purchase goods and services through Ulord and receive payment confirmation quickly, without intervention from any centralized organization. Ulord can easily meet relevant business scenarios for instant payment.  

# Application design and framework implementation  
Considering the bottom “operating system” and the upper “application program”, all people can find their favorite resources in the P2P network through the website released by the publisher to get data from the site directly. This chapter briefly introduces the subsequent application planning and participating process.  

## Main characteristics  

- **Real name system**  
The roles involved in the application platform will involve responsibilities and interests. Only the users who pass the real name verification (KYC) can publish contents, comment or forward in the system, so that they can get the reward of the system. The real name system can better maintain the safety and order of the system.  

- **Content filtering**  
Decentralization does not mean the completely unlimited freedom of speech. For some harmful speech and content (such as pornographic movie), it is necessary to delete and prevent it. In Ulord system, in addition to using AI for vulgar content identification, a consensus-based review mechanism (voting system) is used to allow the public to filter out the inappropriate content.  

- **Cannot be tampered**  
All contents entering the distribution system (final draft and pass consensus review), including the issued comments or forwarding, cannot be tampered. The content timestamp of entering blockchain is used as the basis for the final content copyright confirmation. It is equivalent to establish an evidence system of content publishing and dissemination on blockchain.  

- **Anti-spam mechanism**  
Through the principle of “all contents must be traded”, the amount of spam can be greatly reduced, such as all the pirated or contents with no value. At the same time, through the design of real name system, piracy or other bad behaviors will also make users with “record” in the system which cannot be changed, and affects the user's credit rating.  

- **Incentive mechanism**  
The content user needs to pay some fees (UlordTokens) for contents he needs, and the cost will be automatically assigned to content publisher，disseminator and even high-quality critics with triggering of smart contract. From another perspective, it is equivalent that currency recovery mechanism in economy system to promote monetary circulation in the system.  

- **Transaction between applications**  
Considering long-term design, different application fields may have different tokens; users may also be active in various applications based on this content system, so as to hold all kinds of tokens. In this case, token exchange and cross-application transaction are supported by the mechanism.  

## Distribution mechanism  

![figure10](https://github.com/UlordChain/Document/raw/master/img/figure10.png?raw=true)  

There are four main roles in the platform:  
- Copyright author: copyright owner  
- Spreader: work promoter  
- Consumer: work audience  
- Account recorder: miner  

The authors can upload their works, set the category, fill profile, set content aging, and make price by themselves. According to the classification browsing, the consumers can search their favorite contents and author on the platform, view brief instruction of content and user comment, purchase content, make ratings and comment on the bought contents. Ulord encrypts digital content. Through the accounting system, Ulord finds out the publisher, distributes fees paid by consumers. When the interest distribution is confirmed, you can download the content, and record the data in blockchain. Through Ulord blockchain and data distribution system, digital content can not only be provided directly for consumers, but also can be recommended for spreading according to its own quality and popularity. The spreader distributes the incomes to all parties in accordance with the storage, forwarding and promotion of digital contents.
The main actions in the above process include:  

- **Work publishing**
Work publishing refers to the process of making digital content and uploading to the network by the author. The process is as follows:  
  - a.	Author creates the digital content.  
  - b.	According to the author's application for releasing, Ulord generates AES private key, and encrypts the non-free content. Meanwhile the commands are sent to the node of account recorder;  
  - c.	Ulord generates content submission transaction according to the author's application.  
  - d.	The account recorder downloads the published work and initiates a coverable transaction certificate for confirming that the content has been successfully released.  
  
- **Purchase work**  
Purchase refers to the process that consumers decides to purchase some published work. Purchase takes the form of contract and starts with the promise of consumers' payment, so as to confirm that the account recorder has already distributed the work and the consumer pays to the author. Here are the processes:  

  - a. The consumer chooses the work he wants to buy, and submit purchase application;  
  - b. The purchase application generates a purchase request transaction on the platform, which will effectively freeze the corresponding number of digital coins in the consumer account.  
  - c. After the account recorder node finds purchase applications in blockchain, he will use the private key to decrypt. With the consumer's public key, re-encryption will be carried out; at the same time, the private key distribution trading is generated, including sharing of private key encryption of consumers and delivery certificate;  
  - d. The account recorder pays the fund to the author that is frozen in the consumer account;  
  - e. The consumer will use the private key to decrypt the secret key share to get the work;  
  - f. The consumer can submit a rating transaction in blockchain to score and comment the published work; different rating and classification engines collect these rating transactions, which can take intelligent push of work according to consumers' behaviors and habits.  
  
- **Mining**  
Based on the following considerations:  
  - a.	The enterprise/family computer or other computing resources are not in full use. Owners are eager to share their idle bandwidth resources, storage space and computing resources to make effective using and resources realization.  
  - b.	Users who are involved in storage (they can be rewarded), or users who are consuming work, can also become account recorder of Ulord.  
Ulord designs two kinds of mining nodes, one is common mining node, namely the enterprise/family computer or other equipment. The computer software mining client will be issued without need to spend money to add other equipment to become the account recording node of Ulord to participate in mining after software installation. The mining is divided into the intelligent mining, full speed mining and other mode, so that the home and office computer can be used for more purposes. It can not only meet entertainment needs, but also share resources to earn UlordToken. The other is the professional mining node, which has been mentioned in the original chain design. Mining algorithm is only designed for CPU mining, so we provide professional mining equipment which is different from the currently available GPU mining rig and ASIC mining rig and specific for Ulord accounting. The equipment may be the cloud host of the cloud computing center.   
This mining model is actually optimization of technological innovation resources through scheduling, which reduces social resources consumption, transforms waste into treasure, and is friendly to environment; from the perspective of content distribution and dissemination, UlordToken can be obtained both from sharing of valuable contents and mining.  

![figure11](https://github.com/UlordChain/Document/raw/master/img/figure11.png?raw=true)

- **Spread**   
Only when the spread and using frequency of copyright work is increased, the value of work is likely to rise; the digital content used by no one has no value. In the Internet era, everyone is a content disseminator, and has right to express any ideas of to comment, distribute or reproduce contents; the time and energy paid on them can also be rewarded on Ulord. Therefore, provision and dissemination of high-quality content are encouraged.  

## UlordToken allocation scheme  
UlordToken is Ulord platform cryptocurrency, referred to as ULD, with a total issue of 1 billion, and its circulation will not be increased or destroyed. UlordToken is used as a payment in Ulord, as the currency in Ulord ecosystem. A reasonable allocation of UlordToken is helpful to promote the healthy development of Ulord ecosystem. The distribution mechanism is as follows:  
Ulord team and early investors: 20%, for all the team Ulord members and early investors contribution awards. 10% of them are pre-mining for R & D investment of the previous stage of the project; the remaining 10% has a lock period of 48 months to ensure that the project can advance;   
Community developers: 10%, for promoting the development of community ecology, and helping developers to carry out meaningful development plans. The lock period will not be temporarily set. The reward depends on code review and quality assessment of the development task as well as task process according to community vote;  
PoW: 35%, to motivate the miners to provide more CPU power billing.  
PoS: 25%, to reward master node, and also encourage more users to provide storage space for storing Ulord platform data.  
Community operations and product promotion: 10%, to make the project in the market as soon as possible, 10% of the budget will be used as an early promotion fee. Ulord will try a new model of community autonomy, and all the expense are determined by community volunteers.  

## How to get UlordToken  
There are five ways to get UlordToken:  
- (1)	CPU computing resources involves in accounting;  
- (2)	Server nodes participate in network infrastructure construction;  
- (3)	Community promotion and code contribution;  
- (4)	Publish original internet content;  
- (5)	Spread valuable internet content.  

Among the above, the first three ways are to obtain UlordToken in "production" and the last two ways to get UlordToken in "circulation". UlordToken assets will be recorded on Ulord's wallet. Owning UlordToken means joining the Ulord community, where members and users work together to promote its ecological value.  

# Ulord Team  
Ulord team brings together a large number of high-level R & D personnel led by more than 10 PhDs, with comprehensive blockchain technology application development capabilities. More than 50 excellent programmers and algorithm engineers in the technology development team have backgrounds in areas such as blockchain, cryptography, Internet information security, big data, cloud computing, artificial intelligence, finance, and management. There are senior scientists in cryptography and blockchain, and specialized blockchain project investors. In addition, Ulord team also maintains close cooperation with research institutes such as Windsor University in Canada, Manchester University in the UK, Wuhan University, Beihang University and Chinese Academy of Sciences to jointly develop key technologies in Ulord platform.  

## Core Team  
**Dam Woods**, CEO, PhD，over the past decade he has been committed in research and development of cloud computing, and has a rich experience in leading technical team to explore major projects. He once served as a director of a huge cloud computing center and has unique insights in the blockchain industry.  
**Kwuaint Li**, CTO，PhD，a reliable Chinese programmer. He once worked in Nortel Networks as SME, and devotes himself to researching and promoting blockchain technology. Under the control of blockchain technical risks, he dreames he would bring the technology dividend to the public.   
***Cyber Kuber**, CMO,PhD, one of the earliest investors in blockchain and has actively advocates mastering and marketing this technology. He thinks blockchain will lead people to develop more sophisticated society and Ulord will show its true value in this process.  
**Chaoyun Ting**, PhD in Computer Science and Technology. He mainly engages in artificial intelligence, data mining, network security, blockchain and digital currency and other areas. As one of the earliest domestic scholars engaging in social network research, he is the main founder of the social network open source community. He has 8 national invention patents. His deep interest in computer leads him to discover blockchain and become a leader of data analysis and processing team.                                  
**Yan Xiangtao**, PhD, visiting scholar at the University of Denver in the United States. He has participated and completed 5 items of the national science and technology projects, presided over 3 research project and published more than 30 research papers. He is experienced in project justification, technology development, management coordination and serves as Ulord Project Systems Design Team Leader.  
**Laktic Lattie**, PhD of Computer Science and Technology, graduated from Computer College Wuhan University. He has deep foundation in big data mining, distributed storage technology and other areas, involving in multiple blockchain project researches and developments, and hosts 5 invention patents. He serves as project P2P team leader in Ulord.  
**Cui Lin**, PhD of Computer Science and Technology. He participates in the design and development of large-scale distributed systems. He has deep research and rich practice in cloud computing and artificial intelligence. He serves as AI team leader in Ulord.  
**Zhang Min**, PhD of 6th University, Paris, France, mainly engages in natural language processing and machine learning related algorithms research, is familiar with all kinds of intelligent parallel acceleration and optimization algorithms and has rich practical experience in distributed system fault modeling, user behavior analysis and content recommendation. He serves as AI team member in Ulord.  
**Chen Hu**, PhD, graduated from National University of Defense Technology, Associate Professor of South China University of Technology. He mainly engages in encryption algorithms, information security direction research and implementation,   and serves as encryption algorithm group leader in Ulord.   
**Li Mai**, PhD of University of Windsor, Canada, visiting scholar at McGill University. He has long been engaged in intelligent optimization algorithm design, blockchain and other related research. He serves as encryption algorithm team leader in Ulord.  
**Liang Liang**, PhD of Management Science and Engineering. He has conducted deep research on system evaluation and optimization methods, complex system modeling and blockchain finance, and gained rich experience in system software design and development. He serves as economic model team leader in Ulord.  
**Teh Sunn Liu**, PhD, core algorithm engineer, comes from Chhattisgarh, India. He loves encryption algorithms as much as mountain climbing.  
In addition to the above backbones, there are Li Wenzhou, Zhou Kaiyuan, Zhong Yunhua, Qu Pengcheng, Liu Xiu, Hu Biao, Liu Qi Ping, Liu Bicheng, Su Mingrui, Yang Chang, Guo Lei, Liu Chunjie, Chen Xiaojing, Nie Lang, Hu Qingping, Zeng Xuedong, Chen Jian, He Jin, Wang Lu, Shu Xudong, Guo Taibiao, He Tao, Quan Songlin, Cao Linan, Zou Zhenan, Luo Xi, Chen Yunying, Peng Libiao, Yin Haibo, Peng can, Zhang Lv, He Chao, Liu Yang, Chen Qian, Tan Ke, etc., involved in research and development. They are convinced that the blockchain will bring a new era, and willing to join this technological change.  

## Advisers  
**Chris Wood**, served as an associate professor of computer science and software engineering at a university in Australia, senior researcher and research director, Department of Computer Science and Mathematics, a University in Spain. He is now a top university professor and doctoral tutor in China. His research includes cloud computing security, big data security and privacy, blockchain and digital currency, emerging information systems security and application cryptography.  
**Yu Yong**, Professor, School of Computer Science, Shaanxi Normal University, PhD tutor , professor of Shaanxi Provincial Hundred Talents Program, member of China Cryptography Society Youth Working Committee, China Cryptology Association Working Committee, China Confidentiality Association Privacy Protection Committee. His research includes public key cryptography and applications, blockchain and cryptocurrency, cloud computing security, big data security and privacy protection.  
**Zhang Xiaoming**, PhD of Computer Science and Technology, former member of "High Performance Computing" Innovation Team of National Defense Science and Technology University, now serve as chief architect of Hunan Great Wall Galaxy Science and Technology Co., Ltd. He was former deputy chief designer of "Tianhe" series supercomputer computing and processing system in China.  
**Chen Wenhua**, PhD, University of Alberta, Canada. He has a solid foundation in evolutionary computing, machine learning, big data and other related fields. He served as chair in the intelligent optimization mainstream conferences WCCI, CEC, SSCI and many other organized thematic meetings. He is currently a reviewer for over 10 internationally renowned journals including IEEE TEVC, IEEE TCYB, Information Sciences, Applied Soft Computing.  
**Jack Yi**, LD Capital Founder, a well-known investor in Blockchain, invested in Tianhe Guoyun, Chafta Technology, Guangdong Hulubao Co. Ltd., Jiwei Co. Ltd., 31 Meeting Co. Ltd., Qtum, DEW, Ven, Big1, BeeChat, Mixin, Zcash, EOS, TAMC, AELF, UChain, etc.  
**Feng Tao**, PhD of mathematics, Toronto University. He is currently the founder, president and managing partner of Shanghai Yongxuan Venture Capital Management Co., Ltd. He has been selected as one of "Fortune" global 25 corporate new stars. On December 15, 2009, he was named as "2009 Forbes China's best venture capital investors" by "Forbes" Chinese magazine, and ranked fourth.  
**Cao Wei**, joined Bluerun Beijing Office in November 2010 and currently serves as investment director. His main interests include the Internet community, games, e-commerce and wireless applications.  
**Liu Feng**, FGB partner.  
**Wu Gang**，Bixin CEO.  

## Investment agency  
Tong Dao Uncle, TOPCODE CAPTIAL, DFund, Node Captial, Chain Funder, Link Captail, Jiuding Lab, Hillhouse Captail, Youling Captial, LD Captail, Sparking Star Captail, 007No Quitters, Bixin, Vernacular blockchain.  

# Project promotion plan  
Q4 2016   Start the journey of Ulord ecological construction  
Q2 2017   Achieve the key technology research for public blockchain  
Q3 2017   Complete the basic work of public blockchain, and set up the framework of information resource distribution platform  
Q4 2017   Public blockchain large-scale node test  
Q1 2018   Release Ulord Technical White Paper, Ulord testnet is online  
Q2 2018   Ulord main chain is online, release Ulord platform V1.0, provide application model and business service  
Q3 2018   Launch Ulord master nodes, construct over 10 applications based on Ulord public blockchain  
Q4 2018   Release Ulord platform V2.0, dock more applications and basically build Ulord ecosystem  

# Summary  
After in-depth industry research and technology exploration, we deeply believe that the blockchain technology will open a new window for content distribution industry, and overturn the traditional mode with decentralized, reliable technology and mode to realize the valuable and efficient transmission. Ulord platform integrates the bottom blockchain service and P2P distributed service, providing the overall solution of Internet content distribution based on blockchain for the majority of users. We have the confidence to promote technological innovation and create a perfect ecology based on content distribution application relying on our rich experience in blockchain and P2P technology.  

# Disclaimer  
Blockchain, an emerging industry, with the extremely high investment risk and technical risk, belongs to high risk investment industry. White technical paper, as a technology and product description, describles the prospects of the technology and industry. People who cannot bear the risk is not recommended for investment.  

# Version statement  
When there are contradictions between different versions, the latest version shall prevail.  

# Power of interpretation  
Ulord Foundation reserves the final interpretation of this white technical paper.  
 
# References  
1. Nakamoto, Satoshi (31 October 2008). "Bitcoin: A Peer-to-Peer Electronic Cash System" (PDF). bitcoin.org. Archived (PDF) from the original on 20 March 2014. Retrieved 28 April 2014  
2. EB Sasson, A Chiesa, C Garman. Zerocash: Decentralized Anonymous Payments from Bitcoin. IEEE Symposium on Security & Privacy , 2014 :459-474  
3. A Next-Generation Smart Contract and Decentralized Application Platform. https://github.com/ethereum/wiki/wiki/White-Paper  
4. Ethereum: A Sercure Decentralised Generalised Transaction RANSACTION Ledger.http://gavwood.com/paper.pdf  
5. Dash: A Privacy-Centric Crypto-Currency. https://github.com/dashpay/dash/wiki/Whitepaper  
6. CryptoNote v2.0. https://github.com/monero-project/research-lab/ blob/master/whitepaper/whitepaper.pdf  
7. Kosba A, Miller A, Shi E, et al. Hawk: The Blockchain Model of Cryptography and Privacy-Preserving Smart Contracts[C]// Security and Privacy. IEEE, 2016:839-858  
8. Distributed hash table. https://en.wikipedia.org/wiki/Distributed_hash _table  
9. BitTorrent. https://en.wikipedia.org/wiki/BitTorrent  
10. Wright, A; De Filippi, P. (March 10, 2015). "Decentralized Blockchain Technology and the Rise of Lex Cryptographia". SSRN 2580664?Freely accessible.  
11. Levine, M. (17 May 2016). "Blockchain Company Wants to Reinvent Companies". Bloomberg View: Wall Street. Bloomberg News.  https://www.bitcoinbook.info/translations/cmn/book.pdf   
12. Chao Y, XU M, SI X. Research on A New Signature Scheme on Blockchain[J].  
13. Kalodner H, Goldfeder S, Chator A, et al. BlockSci: Design and applications of a blockchain analysis platform[J]. arXiv preprint arXiv:1709.02489, 2017.  
14. Zeilinger M. Digital art as “monetised graphics”: Enforcing intellectual property on the blockchain[J]. Philosophy & Technology, 2016: 1-27.  
15. Mastering Bitcoin. https://github.com/bitcoinbook/bitcoinbook.  
16. Mastering Ethereum. https://github.com/ethereumbook/ethereum book.  







