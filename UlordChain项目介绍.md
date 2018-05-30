### UlordChain  
介绍：Ulord是一条点对点的价值传递公链，通过搭建区块链底层架构和数字资源分发协议，支持第三方开发商在其开源协议之上构建自己的应用程序，与众多行业合作伙伴一起形成区块链技术与应用的完整生态。  
目的：基于Ulord创建的各种规则和协议，嫁接包括文字、图片、音乐、视频、软件等在内的各类数字资源应用场景，为信息创造者与消费者提供直接的对接平台。  
链接：https://github.com/UlordChain/UlordChain

###	Ulordj-thin  
介绍：ulordj库是Ulord的Java实现，支持交易发送/接收等事务，是一个“精简版”的ulord chain，是Ulord侧链节点所需要的重要组件。  
链接：https://github.com/UlordChain/ulordj-thin  

### Ulord-sidechain  
介绍：Ulord-Sidechain (USC)是Ulord的侧链实现。  
作用：Ulord侧链的目标是让Ulord支持智能合约，即时交易确认、高并发等特性，且具有良好的可扩展性。Ulord侧链与Ulord之间的通信，采用双向锚定技术，通过联合挖矿来奖励Ulord矿工，使他们能够积极参与主链和侧链的记账。  
链接：https://github.com/UlordChain/Ulord-Sidechain  

### node-multi-hashing  
介绍：集成了CryptoHello算法，可以编译js库，应用js前端应用开发。  
链接：https://github.com/UlordChain/node-multi-hashing  

### Uwallet-client-pro  
介绍：自主开发的Ulord轻钱包，采用简单支付验证协议，具有良好的用户体验和吞吐性能，满足生产环境需求。  
链接：https://github.com/UlordChain/uwallet-client-pro  

### Uwallet-服务器  
介绍：Ulord钱包服务器开源实现，支持高并发场景，用于轻钱包与底层区块链的快速交互。  
链接：https://github.com/UlordChain/Uwallet-server  

###	Uwallet  
介绍：Uwallet提供基于spv钱包的抽象接口。可为各个业务层提供钱包的API调用接口，使钱包与业务分离，降低程序耦合。  
链接：https://github.com/UlordChain/Uwallet  

### Ulordrig  
介绍：ulordrig是一个高性能CPU版本的ulord挖矿程序，支持windows、ubuntu和MAC等多操作系统。  
链接： https://github.com/UlordChain/ulordrig  

### UlordChain/bitcore-node-ulord  
介绍：Ulord区块浏览器开源实现，采用Node.js架构，能对外提供区块信息查询服务。  
链接：https://github.com/UlordChain/bitcore-node-ulord  

###	UlordChain/gradle-witness  
介绍：Gradle Witness是一个gradle插件，能对项目中的远程依赖进行静态验证。  
作用：验证项目所需依赖和完整性。  
链接：https://github.com/UlordChain/gradle-witness  

### CrossChain 跨链  
介绍：Ulord CrossChain项目是允许多种加密货币在线交换，不依赖第三方中心化机构。  
作用：Ulord CrossChain模块使用散列时间锁定智能合约，以便在指定时间内进行货币交易，否则交易将被取消。只要支持OP_SHA256和OP_CHECKLOCKTIMEVERIFY，就可以使用。  
链接：https://github.com/UlordChain/CrossChain  

### py-ulord-api  
介绍：Ulord平台的python版本SDK。  
效果：包含创建用户关系数据库，资源数据库等，以及相关的查询，封装了ulord平台的http调用，方便快速创建ulord应用。 
链接：https://github.com/UlordChain/py-ulord-api  

### cryptohello-hash-lib  
介绍：本项目是一个工具，用于将Ulord使用的CryptoHello工作量证明算法，打包成静态数据链接库以及提供给Python使用的动态链接库文件。  
链接：https://github.com/UlordChain/cryptohello-hash-lib  

### ulord-blog-demo  
介绍：基于内容付费的博客平台，通过nodejs中间层、express框架及paython后台搭建的ulord博客开源系统。  
效果：主体分为前台包括用户注册登录面板，文章内容列表以及分页；内容详情页有文章内容展示，文章支付查看，文章的发布页等。  
链接：https://github.com/UlordChain/ulord-blog-demo  

###	ulord-node-stratum-pool  
介绍：Ulord项目的矿池服务，采用了CryptoHello算法。  
作用：基于nodejs v4.8.7 和redis v2.6，即可简单易用的搭建满足生产环境的Ulord矿池。目前已经有上10个矿池采用该资源对外服务，支持的总算力超过120M，用户数超过10000，矿机连接数超过10万，具有良好的横向和纵向扩展性。  
链接：https://github.com/UlordChain/ulord-node-stratum-pool  

### node-stratum-pool  
介绍：基于Nodejs的Ulord矿池核心库，实现了区块打包、交易验证、任务分发及收益结算等功能。  
作用：支持多种币种，集成了CryptoHello算法。  
链接：https://github.com/UlordChain/node-stratum-pool  

### Uschema 
介绍：Uschema是用于应用内容上链的数据格式化模块。  
作用：用于定义在Ulord区块链中数据声明结构和数据验证方式，支持代码构建和解析。它用于定义数据的格式并在Ulord区块链中对其进行验证。  
链接：https://github.com/UlordChain/Uschema  

### Ulord -platform
介绍：Ulord平台是一个提供内容上链，内容在线支付和内容搜索等功能的去中心化内容分发平台，使得企业更有效率地开发面向内容分发领域的应用。  
作用：Ulord平台软件使开发人员能够创建和部署高性能，可扩展的区块链基础架构。 此代码目前是alpha级质量并处于快速发展阶段。  
链接：https://github.com/UlordChain/Ulord-platform

### bitcore-lib-ulord  
介绍：基于Ulord的JavaScript 库，支持Ulord地址生成、签名、多重签名等功能，可用钱包、区块链浏览器等多种应用。  
链接：https://github.com/UlordChain/bitcore-lib-ulord  

### insight-api-ulord  
介绍：用于Ulord区块链 API接口服务，对外提供第三方公共API  
链接：https://github.com/UlordChain/insight-ui-ulord  

### uwallet-client  
介绍：Uwallet桌面版轻钱包，采用SPV协议，能用于交易发送、交易接收及交易签名等，采用标准的BIP-39协议。  
链接：https://github.com/UlordChain/uwallet-client  

### insight-ui-ulord  
介绍：Ulord区块浏览器的开源实现，支持一键部署，满足生产环境。  
链接：https://github.com/UlordChain/insight-ui-ulord  

### Document  
介绍：Ulord的文档归类，包括算法实现、技术白皮书等。  
链接：https://github.com/UlordChain/Document  

### Ulord Miner Desktop
介绍：Ulord挖矿客户端，提供用户友好设置界面，能实时展示挖矿性能。  
资源链接： https://github.com/UlordChain/UlordMiner-Desktop



   





