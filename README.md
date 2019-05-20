# Reinvent-Mall

从零造的电商系统，用于个人实践与 NGTE 教学。其技术理论依托于 [服务端应用程序开发与系统架构/微服务架构与实践](https://github.com/wx-chevalier/Backend-Series) 等系列文章。

核心的电商相关数据库定义参考 [mysql-ecommerce https://url.wx-coder.cn/Lmzp3](https://url.wx-coder.cn/Lmzp3)，本仓库主要包含以下模块：

- [server](): 核心的服务端相关模块。

- [client | 客户端](): 分别包含 [Web]()，[Mobile]()，[Weapp 微信小程序]()等。

- [admin | 管理端](): 管理端界面。

- [ha](): 高可用架构的一些实践。

- [deploy](): 基于 Docker 单机、Swarm 以及 K8S 部署的脚本。

此外本仓库还依赖于笔者的其他模块，[Legoble](https://github.com/wx-chevalier/Legoble) 提供了可配置化的界面构建能力。

# Motivation & Credits

- [mall](https://github.com/macrozheng/mall): mall 项目是一套电商系统，包括前台商城系统及后台管理系统，基于 SpringBoot+MyBatis 实现。
