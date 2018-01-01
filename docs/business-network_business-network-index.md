# 开发业务网络

开发商使用Hyperledger Composer来数字化业务网络。业务网络由网络中的多个参与者访问，其中一些参与者可能负责维护（托管）网络本身，称为网络维护者。

通常，网络的每个维护者会运行几个peer节点（用于崩溃容错），并且Hyperledger Fabric跨peer节点复制分布式账本。

## 模型

开发人员与业务分析师合作，为业务网络定义领域数据模型。数据模型使用[Composer建模语言](reference_cto_language.md)进行表示，并定义存储在账本上或作为交易处理的资源结构。

一旦领域模型就位，开发人员就可以用JavaScript编写可执行的交易处理器函数，来实现*智能合约*。

## 访问控制

与此同时，开发者或技术分析师可以定义业务网络的访问控制规则，强制哪些参与者可以访问账本上的数据以及在哪些条件下访问。

## 部署

开发人员将模型、脚本和访问控制规则打包到可部署的*业务网络档案*中，并使用命令行工具将档案部署到运行时进行测试。

## 测试

像所有的业务逻辑一样，为业务网络创建单元和系统测试也很重要。开发人员可以使用流行的JavaScript测试框架（如Mocha和Chai）运行单元测试（针对Node.js嵌入式运行时），或者针对Hyperledger Fabric运行系统测试。

## 集成

一旦业务网络经过测试并到位，就需要创建前端应用程序。使用REST服务器为业务网络自动生成REST API，然后使用Yeoman代码生成器生成Angular应用程序。

REST服务器可以配置为对业务网络中的参与者进行身份验证，确保强制执行凭据和权限。

# 参考

- [**建模语言**](reference_cto_language.md)
- [**访问控制语言**](reference_acl_language.md)
- [**交易处理器函数**](reference_js_scripts.md)