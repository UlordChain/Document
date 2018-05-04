![ulord](https://github.com/binbinErices/Car_CRM_System/blob/master/img/ulord.png?raw=true)

 
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
  - [UlordToken allocation scheme](#ulordToken-allocation-scheme)  
  - [How to get UlordToken](#how-to-get-ulordToken)  
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


