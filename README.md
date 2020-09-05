# JAVA后端开发学习路线
列表来自[CodeSheep](https://space.bilibili.com/384068749)的思维导图，可到其公众号下载xmind文件，也可看他的梳理视频[BV1GQ4y1N7HD](https://www.bilibili.com/video/BV1GQ4y1N7HD)。

持续更新中。。。

------

#   1编程基础

###      1.1 Java语言

####          1.1.1语言基础

​              [基础语法](https://github.com/swing0/java_back_end_study/blob/master/java_basics/JAVA%E5%90%8E%E7%AB%AF%E5%BC%80%E5%8F%91%E8%B7%AF%E7%BA%BF%E2%80%94%E2%80%94%E5%9F%BA%E7%A1%80%E8%AF%AD%E6%B3%95%E7%AF%87.md)

​              面向对象

​              接口

​              容器

​              异常

​              泛型

​              反射

​              注解

​              I/O

​              图形化（如Swing）

####          1.1.2 JVM

​              类加载机制

​              字节码执行机制

​              jvm内存模型

​              GC垃圾回收

​              jvm性能监控与故障定位

​              jvm调优

####          1.1.3并发/多线程

​              并发编程基础

​              线程池

​              锁

​              并发容器

​              原子类

​              juc并发工具类

###      1.2数据结构和算法

####          1.2.1数据结构

​              字符串

​              数组

​              链表

​              二叉树

​              堆、栈、队列

​              哈希

####          1.2.2算法

​              查找

​              排序

​              贪心

​              分治

​              动态规划

​              回溯

###      1.3计算机网络

​               ARP协议

​               IP/ICMP协议

​               TCP/UDP协议

​               DNS/HTTP/HTTPS协议

​               Session/Cookie

###      1.4数据库/SQL

​               SQL语句书写

​               SQL语句优化

​               事务以及隔离级别

​               索引

​               锁

###      1.5操作系统

​               进程/线程

​               并发/锁

​               内存管理和调度

​               I/O原理

###      1.6设计模式

​               单例

​               工厂

​               代理

​               策略

​               模板方法

​               观察者

​               适配器

​               责任链

​               建造者

##   2开发工具

###      2.1集成开发环境

​               Eclipse

​               IDEA

​               VSCode

###      2.2 Linux系统

​               Linux常用命令

​               基本Shell脚本

###      2.3代码管理工具

​               Git

​               SVN

###      2.4项目管理/构建工具

​               Maven

​               Gradle

#   3应用框架

###      3.1后端

####          3.1.1 Spring家族

​              Spring

​                  IOC

​                  AOP

​              SpringMVC

​              SpringBoot

​                  自动配置、开箱即用

​                  整合Web

​                  整合数据库（事务问题）

​                  整合权限

​                     Shiro

​                     SpringSecurity

​                  整合各种中间件

​                     缓存

​                     MQ

​                     RPC框架

​                     NIO框架

​                     等。。。

####          3.1.2服务器软件

​              Web服务器

​                  Nginx

​              应用服务器

​                  Tomcat

​                  Jetty

​                  Undertow

####          3.1.3 中间件

​              缓存

​                  Redis

​                     5大数据类型

​                     事务

​                     消息通知

​                     管道

​                     持久化

​                     集群

​                  memcache

​              消息队列

​                  RocketMQ

​                  RabbitMQ

​                  Kafka

​              RPC架构

​                  Dubbo

​                  GRPC

​                  Thrift

​                  SpringCloud

​                  Netty

####          3.1.4数据库

​              ORM层框架

​                  MyBatis

​                  Hibernate

​                  JPA

​              连接池

​                  Druid

​                  HikariCP

​                  C3P0

​              分库分表

​                  MyCat

​                  Sharding-JDBC

​                  Sharding-Sphere

####          3.1.5搜索引擎

​              Solr

​              ElasticSearch

####          3.1.6分布式/微服务

​              服务发现/注册

​                  Eureka

​                  Consul

​                  Zookeeper

​                  Nacos

​              网关

​                  Zuul

​                  Gateway

​              服务调用（负载均衡）

​                  Ribbon

​                  Feign

​              熔断/降级

​                  Hystrix

​              配置中心

​                  Config

​                  Apollo

​                  Nacos

​              认证和鉴权

​                  Shiro

​                  SpringSecurity

​                  OAuth2

​                  SSO

​              分布式事务

​                  JTA接口

​                     Atomikos组件

​                  2PC、3PC

​                  XA模式

​                  TCC模式

​                     tcc-transaction

​                     ByteTCC

​                     EasyTransaction

​                     Seata

​                  SAGA模式

​                     ServiceComb

​                     Seata

​                  LCN模式

​                     tx-lcn

​              任务调度

​                  Quartz

​                  Elastic-Job

​              链路追踪与监控

​                  Zipkin

​                  Sleuth

​                  Skywalking

​              日志分析与监控

​                  ELK

​                     ElasticSearch

​                     Logstash

​                     Kibana

​              虚拟化/容器化

​                  容器技术

​                     Docker

​                  容器编排技术

​                     Kubernetes

​                     Swarm

###      3.2前端

####          3.2.1基础套餐

​              三大件

​                  HTML

​                  Javascript

​                  CSS

​              基础库

​                  Jquery

​                  Ajax

####          3.2.2模板框架

​              JSP/JSTL

​              Thymeleaf

​              FreeMarker

####          3.2.3组件化框架

​              Node

​              VUE

​              React

​              Angular

##   4运维知识

###      4.1 Web服务器

​           Nginx

###      4.2应用服务器

​           Tomcat

​           Jetty

​           Undertow

###      4.3 CDN加速

###      4.4持续集成/持续发布

​           Jenkins

###      4.5代码质量检查

​           sonar

###      4.6日志收集/分析

​           ELK

##   5成神之路

​       徒手撕源码

​       光脚造轮子

​       闭眼深优化

​       吊打面试官

##   6平稳降落

​       调节心态、注意健康

​       虚心学习

​       持之以恒
