---
layout: default
---

![王亚伦照片](/assets/images/jianli.jpg){: style="width:150px; float:right; margin:10px 30px 0px 0px;" }

# 王亚伦（Java 开发工程师）

- 📱 电话：17887313483  
- 📧 邮箱：[3213073759@qq.com](mailto:3213073759@qq.com)  
- 🔗 GitHub：[xiaoluncode](https://github.com/xiaoluncode)   
- 🏠 籍贯：江苏·扬州  
- 🎂 年龄：22  

---

## 教育背景

**南京邮电大学通达学院**（2021.09 – 2025.06）  
本科 · 软件工程  
- 主修：Java 程序设计、数据结构、算法分析与设计、Linux 编程、C 语言、C++  
- 英语：CET-4  

---

## 专业技能

- **Linux & Shell**：熟悉 Linux 操作系统，了解常用 Linux 基本指令，shell 脚本的编写，能够实现 nginx+keepalived 高可用性负载均衡集群搭建；
- **容器化**：能基于 docker、k8s 技术进行容器化应用的集群搭建，了解 zabbix 监控系统；  
- **数据库**：熟练关系型数据库如 MySQL、Oracle 的语法，掌握多表联查和子查询，熟悉SQL优化，索引、事务，深入了解B+Tree索引结构，事务四大特性，三个并发问题，四种隔离级别；  
- **缓存**：了解 Redis 缓存,熟悉数据类型,缓存持久化,对缓存雪崩、缓存击穿、缓存穿透有所了解； 
- **Java 集合**：熟悉常用系统类和集合体系，掌握 ArrayList、LinkedList 实现原理，了解 HashMap 底层工作原理，掌握并发集合类如 ConcurrentHashMap 以确保线程安全；
- **并发**：熟悉并发编程知识,如线程的调度方法、多线程创建的方式、线程池的核心参数，了解同步锁 synchoronized 的锁升级过程，读写锁的锁降级过程，volatile 关键字；  
- **前端**：了解 html、css、js，用 Vue+ElementUI 等组件编写前端页面, Axios 技术调用后端API；  
- **后端**：熟悉 Spring 框架中的 IOC、AOP,了解MVC架构思想,能够使用 SpringBoot 完成对 Mybatis、MybatisPlus、Redis、Minio 等的整合,了解 SpringBoot 的工作原理；
- **微服务**：了解 Spring-Cloud 微服务/分布式架构，熟悉使用 Nacos、OpenFeign、Sentinel、Gateway、Seata 等组件,了解流控、熔断、热点等规则；
- **工具链**：熟悉 Maven 管理构建工具和 git 的基本使用如合并分支,远程推送,能够多人合作使用远程仓库进行开发；  

---

## 项目经历 

### SaaS 多租户微服务管理系统
**技术栈：**Spring Boot 3 · Spring Cloud Alibaba（Nacos · Sentinel · Gateway · OpenFeign）· MyBatis-Plus · Seata · Redis · Spring Security · MinIO · Docker·Kubernetes

**项目简介：**  
基于 SpringBlade Cloud 版本深度定制搭建的企业级 SaaS 平台，内置多租户隔离、分布式事务、流控熔断、统一网关、安全鉴权等微服务基础能力，支持租户在线注册、动态扩容与灰度发布。

**主要职责：**
1. **多租户核心框架**
   - 实现「共享库/共享表」与「独立库/独立表」两种隔离策略，可按业务场景灵活切换；
2. **统一网关与路由**
   - 基于 Spring Cloud Gateway 实现全局路由转发、鉴权拦截与动态限流；
3. **配置与注册中心**
   - 集成 Nacos 作为服务注册与配置中心，支持租户级别的隔离配置和灰度发布；
4. **分布式事务与消息丢失解决方案**
   - 利用 Seata TCC 模式解决跨服务事务一致性，使用 RabbitMQ 消息队列尽可能保证消息不丢失；
5. **安全与鉴权**
   - 基于 Spring Security + JWT 实现统一认证，细粒度控制租户、角色、权限；
6. **运维与容器化**
   - 使用 Docker 镜像构建、Kubernetes 编排部署

**核心亮点：**
- **动态租户路由**：租户标识自动映射到对应数据源或数据表，无需侵入业务代码；
- **高可用网关**：基于 Sentinel 实现流量熔断、热点限流，支持请求链路追踪；
- **可插拔模块**：所有业务微服务按模块化设计，插件式接入，按需按版本更新。

### 智能电影推荐与多维评论分析平台  
**技术栈**：Vue3 · Element Plus · Axios  |  SpringBoot3 · MyBatis-Plus· MySQL · Redis  

**主要职责**  
1. **登录模块**  
   - 分为管理员和普通用户角色，用户成功登录会生成一个token并设置动态过期时间，存储于 Redis、cookie客户端、session服务器端中，再次访问时url请求携带未过期token可以跳过登录界面； 
2. **系统首页**  
   - 分页展示电影排行榜和公告信息，电影排名通过电影平均评分、情绪评分、评论数归一化实现排行榜
3. **影评管理**  
   - CRUD、支持多维度筛选与排序  
4. **信息管理**  
   - 实现电影分类、电影详情和系统公告的信息管理功能，对大批量数据处理的关键节点设置异常捕获机制。

**核心解决方案**  
- **防重复提交**：短期 Token+Redis 拦截器限流，接口防抖  
- **批量导入线程安全**：ReentrantLock+线程池 + MySQL 事务  
- **模糊查询瓶颈**：前缀索引 + Redis 缓存，查询性能提升 

---

## 自我评价

- 编程热情高，关注IT前沿技术，熟练使用开发工具，对AI大模型等感兴趣 
- 具备良好的团队沟通协调能力，执行力
- 工作认真负责，具备加班意愿

---

> **访问**：  
> https://xiaoluncode.github.io/  

