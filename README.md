# Reinvent-Mall

从零造的电商系统，用于个人实践与 NGTE 教学。其技术理论依托于[服务端应用程序开发与系统架构/微服务架构与实践](https://github.com/wx-chevalier/Backend-Series)，[深入浅出分布式基础架构](https://github.com/wx-chevalier/Distributed-Infrastructure-Series)等系列文章。

核心的电商相关数据库定义参考 [mysql-ecommerce](https://url.wx-coder.cn/Lmzp3)，本仓库主要包含以下模块：

- [modules](): 核心的服务端相关模块。

- [client | 客户端](): 分别包含 [Web]()，[Mobile]()，[Weapp 微信小程序]()等。

- [admin | 管理端](): 管理端界面。

- [ha](): 高可用架构的一些实践。

- [deploy](): 基于 Docker 单机、Swarm 以及 K8S 部署的脚本。

此外本仓库还依赖于笔者的其他模块，[Legoble](https://github.com/wx-chevalier/Legoble) 提供了可配置化的界面构建能力。

# Preface | 前言

现代电商系统是一系列业务域、功能域与服务域的组合，域本身是领域建模过程中，针对目标领域中设计到所有业务实体及其服务，按照一定的原则进行的归类。

- 功能域：功能域会对外提供可供系统连接、流程编排的功能服务接口，每个功能是为了达到某个独特的商业目的而提供的数据模型、业务流程与衡量标准的组合。功能域的核心特点是对外屏蔽内部具体实现的依赖关系，以方便在不同的商业模型下灵活切换。譬如在云制造场景下，前端业务无须关注具体的制造车间（即店铺与库存）。功能域同样需要提供强大的可扩展能力，规范化可扩展点，允许第三方在系统调用中进行灵、可配置地扩展。

- 业务域：业务域包含了一系列面向最终用户的业务。业务域是对于能力中台提供的一系列基础能力的组合，这些组合会形成某个业务具体的商业能力，最终助力达成业务目标。

- 系统域：系统域类似于业务域，是基于各个功能域提供的服务进行逻辑编排之后的系统执行次序的组合能力。系统域典型的落地场景即是管理中台。

- 服务域：服务域提供了独立于业务逻辑、商业模式之外的通用能力，以接口、MQ 等方式暴露使用。服务域典型的落地场景即是数据中台，主体面向数据本身提供搜索、指标、报表等能力。

![](https://i.postimg.cc/65zCBvqk/image.png)


# Home & More | 延伸阅读

![](https://i.postimg.cc/59QVkFPq/image.png)

您可以通过以下导航来在 Gitbook 中阅读笔者的系列文章，涵盖了技术资料归纳、编程语言与理论、Web 与大前端、服务端开发与基础架构、云计算与大数据、数据科学与人工智能、产品设计等多个领域：

- 知识体系：《[Awesome Lists](https://ngte-al.gitbook.io/i/)》、《[Awesome CheatSheets](https://ngte-ac.gitbook.io/i/)》、《[Awesome Interviews](https://github.com/wx-chevalier/Awesome-Interviews)》、《[Awesome RoadMaps](https://github.com/wx-chevalier/Awesome-RoadMaps)》、《[Awesome MindMaps](https://github.com/wx-chevalier/Awesome-MindMaps)》、《[Awesome-CS-Books-Warehouse](https://github.com/wx-chevalier/Awesome-CS-Books-Warehouse)》

- 编程语言：《[编程语言理论](https://ngte-pl.gitbook.io/i/)》、《[Java 实战](https://ngte-pl.gitbook.io/i/java/java)》、《[JavaScript 实战](https://ngte-pl.gitbook.io/i/javascript/javascript)》、《[Go 实战](https://ngte-pl.gitbook.io/i/go/go)》、《[Python 实战](https://ngte-pl.gitbook.io/i/python/python)》、《[Rust 实战](https://ngte-pl.gitbook.io/i/rust/rust)》

- 软件工程、模式与架构：《[编程范式与设计模式](https://ngte-se.gitbook.io/i/)》、《[数据结构与算法](https://ngte-se.gitbook.io/i/)》、《[软件架构设计](https://ngte-se.gitbook.io/i/)》、《[整洁与重构](https://ngte-se.gitbook.io/i/)》、《[研发方式与工具](https://ngte-se.gitbook.io/i/)》

* Web 与大前端：《[现代 Web 开发基础与工程实践](https://ngte-web.gitbook.io/i/)》、《[数据可视化](https://ngte-fe.gitbook.io/i/)》、《[iOS](https://ngte-fe.gitbook.io/i/)》、《[Android](https://ngte-fe.gitbook.io/i/)》、《[混合开发与跨端应用](https://ngte-fe.gitbook.io/i/)》

* 服务端开发实践与工程架构：《[服务端基础](https://ngte-be.gitbook.io/i/)》、《[微服务与云原生](https://ngte-be.gitbook.io/i/)》、《[测试与高可用保障](https://ngte-be.gitbook.io/i/)》、《[DevOps](https://ngte-be.gitbook.io/i/)》、《[Node](https://ngte-be.gitbook.io/i/)》、《[Spring](https://ngte-be.gitbook.io/i/)》、《[信息安全与渗透测试](https://ngte-be.gitbook.io/i/)》

* 分布式基础架构：《[分布式系统](https://ngte-infras.gitbook.io/i/)》、《[分布式计算](https://ngte-infras.gitbook.io/i/)》、《[数据库](https://ngte-infras.gitbook.io/i/)》、《[网络](https://ngte-infras.gitbook.io/i/)》、《[虚拟化与编排](https://ngte-infras.gitbook.io/i/)》、《[云计算与大数据](https://ngte-infras.gitbook.io/i/)》、《[Linux 与操作系统](https://ngte-infras.gitbook.io/i/)》

* 数据科学，人工智能与深度学习：《[数理统计](https://ngte-aidl.gitbook.io/i/)》、《[数据分析](https://ngte-aidl.gitbook.io/i/)》、《[机器学习](https://ngte-aidl.gitbook.io/i/)》、《[深度学习](https://ngte-aidl.gitbook.io/i/)》、《[自然语言处理](https://ngte-aidl.gitbook.io/i/)》、《[工具与工程化](https://ngte-aidl.gitbook.io/i/)》、《[行业应用](https://ngte-aidl.gitbook.io/i/)》

* 产品设计与用户体验：《[产品设计](https://ngte-pd.gitbook.io/i/)》、《[交互体验](https://ngte-pd.gitbook.io/i/)》、《[项目管理](https://ngte-pd.gitbook.io/i/)》

* 行业应用：《[行业迷思](https://github.com/wx-chevalier/Business-Series)》、《[功能域](https://github.com/wx-chevalier/Business-Series)》、《[电子商务](https://github.com/wx-chevalier/Business-Series)》、《[智能制造](https://github.com/wx-chevalier/Business-Series)》

此外，前往 [xCompass](https://wx-chevalier.github.io/home/#/search) 交互式地检索、查找需要的文章/链接/书籍/课程；或者在在 [MATRIX 文章与代码索引矩阵](https://github.com/wx-chevalier/Developer-Zero-To-Mastery)中查看文章与项目源代码等更详细的目录导航信息。最后，你也可以关注微信公众号：『**某熊的技术之路**』以获取最新资讯。

# Motivation & Credits

- [mall](https://github.com/macrozheng/mall): mall 项目是一套电商系统，包括前台商城系统及后台管理系统，基于 SpringBoot+MyBatis 实现。
