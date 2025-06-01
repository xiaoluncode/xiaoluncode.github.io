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
- **工具链**：熟悉 Maven 管理构建工具和 git 的基本使用如合并分支,远程推送,能够多人合作使用远程仓库与团队配合协助进行开发；

---

## 项目经历

### 保险产品分销系统
**技术栈：**Vue + Element Plus + Axios ｜ SpringBoot + Mybatis-Plus + MySQL + Redis + Spring Cloud Alibaba（Nacos、Sentinel、OpenFeign）

**项目简介：**  
本项目为保险分销平台，支持保险公司产品配置管理、顾客投保、核保/出单、多级分销佣金计算、代理人年度业绩统计等核心功能。系统采用前后端分离架构，后端微服务间通过 OpenFeign + Nacos 实现注册发现，Sentinel 进行流量控制。

**主要职责：**
1. 构建订单流程控制引擎
   - 设计订单状态机管理“待核保→核保成功→待支付→支付成功→待出单→已出单”状态流转，避免状态紊乱、流程异常；
2. 自行设计多级分销佣金规则
   - 支持不同险种、分销渠道、代理等级和团队奖励下的佣金策略匹配计算；
3. 热点数据快速展示
   - 使用 Redis 缓存热点产品信息，减少数据库压力；
4. 微服务组件集成
   - Nacos 做配置中心与服务注册发现，Sentinel 实现限流熔断机制保障系统高可用，OpenFeign 做微服务间调用。

**核心解决方案：**
- **多级缓存架构**：采用 Caffeine 实现本地缓存，缓存热点保险产品信息，并采用 LRU 淘汰策略，Redis 存储所有产品信息；使用延迟双删保证缓存与数据库最终一致性；
- **订单状态机设计**：通过状态流转实现订单全生命周期的有效管理；
- **年度业绩查询 SQL 优化**：由原来全表扫描多条记录耗时 4s 缩短至 0.5s。

---

### 智能电影推荐与多维评论分析平台（个人独立开发）
**技术栈：**Vue3 · Element Plus · Axios ｜ SpringBoot3 · MyBatis-Plus · MySQL · Redis

**主要职责**
1. 登录模块
   - 分为管理员和普通用户角色，用户登录后生成 token 存储于 Redis、cookie、session，多端同步管理；
2. 系统首页
   - 展示电影排行榜及公告信息，电影排名基于平均评分+情绪评分+评论量归一化加权计算；
3. 影评管理
   - 实现 CRUD 操作，支持多维筛选与排序；
4. 信息管理
   - 支持电影分类、详情、系统公告等模块管理，处理大批量数据异常捕获。

**核心解决方案**
- 防重复提交：短期 Token+Redis 限流，接口防抖；
- 批量导入线程安全：ReentrantLock+线程池+事务；
- 模糊查询性能优化：前缀索引 + Redis 缓存，实现毫秒级响应。

---

## 自我评价

- 编程热情高，关注IT前沿技术，熟练使用开发工具，对AI大模型等感兴趣；
- 工作认真负责，具备加班意愿，具备良好的团队沟通协调能力与执行力；
- 关注IT技术社区，熟悉若依、Spring Blade等开源框架。

---

> **访问主页：**  
> [https://xiaoluncode.github.io/](https://xiaoluncode.github.io/)
