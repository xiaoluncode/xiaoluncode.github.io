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

### RuoYi-Cloud 微服务平台（开源二次开发）

**技术栈：**Spring Boot 2.7 · Spring Cloud Alibaba（Nacos · Sentinel · Gateway · OpenFeign）· MyBatis-Plus · Seata · Redis

**项目简介：**  
基于开源 RuoYi-Cloud 架构二次开发，支持微服务注册、配置中心、鉴权网关、分布式事务、链路追踪等。

**主要职责：**
1. **服务网关与鉴权**
   - 基于 Gateway 实现全局路由转发、限流；
   - 用户鉴权：外部鉴权（AOP 面向切面 ，基于注解进行环绕增强）+内部鉴权（内部微服务之间调用，若请求头携带 inner 标识，放行）
2. **配置中心 & 注册中心**
   - 采用 Nacos 实现动态配置和服务发现，编写配置刷新脚本。
3. **熔断降级**
   - 集成 Sentinel 实现熔断、限流策略，防止雪崩。
4. **分布式事务与分表**
   - 基于 Seata 实现事务一致性。
5. **第三方登录授权**
   - 集成just-auth实现第三方授权登录，支持Github、Gitee、微博等第三方平台的授权登录。
6. **集成knife4j**
   - 整合knife4j实现swagger文档增强：接口排序，在线调试，文档清晰，注解增强。

**核心亮点：**
- **分库分表**：热点数据单独拆出一张表。
- **高可用微服务治理**：集成 Nacos、Sentinel、SkyWalking、Seata 等组件，系统高可用。


---

### SpringBlade多租户微服务管理系统（开源二次开发）
**技术栈：**Spring Boot 3 · Spring Cloud Alibaba（Nacos · Sentinel · Gateway · OpenFeign）· MyBatis-Plus · Seata · Redis · MinIO · Docker·Kubernetes

**项目简介：**  
基于 SpringBlade Cloud 版本搭建的 SaaS 平台，内置多租户隔离、分布式事务、流控熔断、统一网关、安全鉴权等微服务基础能力。

**主要职责：**
1. **统一网关与路由**
   - 基于 Spring Cloud Gateway 实现全局路由转发、鉴权拦截与动态限流；
2. **统一网关 & 流控限流**
   - 基于 Gateway 实现全局路由转发；
   - 集成 Sentinel，配置热点参数限流与熔断规则，结合 Nacos 做动态规则推送；
3. **分布式事务与消息丢失解决方案**
   - 在跨服务场景使用 Seata TCC，使用 RabbitMQ 消息队列尽可能保证消息不丢失；
4. **安全与鉴权**
   - 基于 Spring Security + JWT 实现统一认证，细粒度控制租户、角色权限；

**核心亮点：**
- **动态租户路由**：租户标识自动映射到对应数据源或数据表，无侵入业务代码；
- **高可用系统**：基于 Sentinel 实现流量熔断、热点限流；
- **可插拔模块**：所有业务微服务按模块化设计，插件式接入，按需加载，降低耦合。

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

