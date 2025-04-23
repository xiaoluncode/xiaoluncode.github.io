---
layout: default
---

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

- **Linux & Shell**：熟悉常用指令、shell 脚本，能搭建 `nginx+keepalived` 高可用负载均衡集群  
- **容器化**：Docker、K8s 集群部署，了解 Zabbix 监控  
- **数据库**：MySQL、Oracle 语法；深刻理解索引（B+Tree）、事务（ACID）、隔离级别与并发问题；SQL 优化  
- **缓存**：Redis 持久化、缓存雪崩/穿透/击穿防护  
- **Java 集合 & 并发**：ArrayList/LinkedList/HashMap 原理；ConcurrentHashMap、线程池、锁模型（synchronized、volatile）  
- **前端**：HTML/CSS/JS + Vue3 + Element Plus + Axios  
- **后端**：Spring IOC/AOP/MVC，SpringBoot + MyBatis(MyBatis-Plus)、Redis、Minio 集成；  
- **微服务**：Nacos、OpenFeign、Sentinel、Gateway、Seata；流量控制、熔断、热点规则  
- **工具链**：Maven、Git/Gitee 协作  

---

## 项目经历

### 智能电影推荐与多维评论分析平台  
**技术栈**：Vue3 · Element Plus · Axios  |  SpringBoot3 · MyBatis · MySQL · Redis  

**主要职责**  
1. **登录模块**  
   - 分为管理员和普通用户角色，用户成功登录会生成一个token并设置动态过期时间，存储于 Redis、cookie客户端、session服务器端中，再次访问时url请求携带未过期token可以跳过登录界面； 
2. **系统首页**  
   - 分页展示电影排行榜和公告信息，电影排名通过电影平均评分、基于NLP库处理的情绪评分、评论数加权计算评分实现排行榜
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

- 编程热情高，关注 IT 前沿技术，快速自驱学习并落地  
- 逻辑清晰，执行力强，团队中甘于承担  
- 工作认真负责，具备加班意愿  

---

> **访问**：  
> https://xiaoluncode.github.io/  

