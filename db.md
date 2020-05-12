## 数据库系统(Database System)资料

- [书籍](#书籍)
- [课程](#课程)
- 进程管理
- [查询/优化器](#查询/优化器)
- [存储](#存储)
- [事务](#事务)
- 共享组件
- [关系模型](#关系模型)
- [NewSQL](#NewSQL)
- [学者](#学者)
- [其他](#其他)



#### 书籍

- [《Database System Concepts》](https://kakeboksen.td.org.uit.no/Database%20System%20Concepts%206th%20edition.pdf)

介绍：经典书籍，数据库系统概念。数据库领域的殿堂级作品。夯实数据库理论基础，增强数据库技术内功的必备之选。内容涉及很广：表、SQL、关系模型、事务、数据库设计、分布式、存储、索引、查询处理与优化、并发、数据库分析（postgresql,SQL server）。书的难度系数对于刚刚入门的同学可能不太适合，但可以当作"词典”。配套书籍[网站](https://www.db-book.com/).

- [《A First Course in Database Systems》](http://infolab.stanford.edu/~ullman/fcdb.html)

介绍：经典书籍，数据库系统基础教程。讲述关系数据模型、ER图、约束与触发器、SQL、视图。适合入门数据库系统的同学。

- [《Architecture of a Database System》](http://db.cs.berkeley.edu/papers/fntdb07-architecture.pdf)

介绍：剖析数据系统内部架构，本文一共包括 8 章，分别是：第 1 章概述，第 2 章进程模型，第 3 章并行体系结构：进程和内存协调，第 4 章关系查询处理器，第 5 章存储管理，第 6 章事务：并发控制和恢复，第 7 章共享组件，第 8 章结束语。[中文版](http://dblab.xmu.edu.cn/wp-content/uploads/old/files/linziyu-Architecture%20of%20a%20Database%20System(Chinese%20Version)-ALL.pdf)由厦门大学数据库实验室翻译

- [《Readings in Database Systems, 5th Edition》](http://www.redbook.io/)

介绍：数据库领域红宝书重出江湖。《Readings in Database Systems, 5th Edition》评注版 Peter Bailis, Joseph M. Hellerstein, Michael Stonebraker编著。十年之后，内容大变，传统数据库架构彻底重写，bigdata浪潮影响深远，数据库领域必看书籍。里面包含有数据挖掘、查询优化、数据库语言.

- [《Database System Implementation》](http://infolab.stanford.edu/~ullman/dbsi.html)

介绍：斯坦福大学本科教材，这本阐述了实现关系数据库系统各个层面的关键技术。主要分为三部分：存储管理器、查询处理器和事务管理器的实现技术。书中从存储，Index，SQL compiler，optimizer, log，事务等关键技术。不太适合数据库入门初学者，理论很多信息量大。[英文版](https://people.inf.elte.hu/miiqaai/elektroModulatorDva.pdf)

#### 课程

- [《CMU 15-721 (SPRING 2018) Advanced Database Systems》](https://15721.courses.cs.cmu.edu/spring2018/)

介绍：卡内基梅隆2018年春季高级数据库课程，对现代数据库管理系统内部的全面研究。它将涵盖高性能事务处理系统（OLTP）和大规模分析系统（OLAP）中的组件核心概念和基础知识。它的[阅读列表](https://15721.courses.cs.cmu.edu/spring2018/schedule.html#jan-24-2018)、[课堂笔记](https://15721.courses.cs.cmu.edu/spring2018/notes/)、[课件](https://15721.courses.cs.cmu.edu/spring2018/slides/)都已经开放。并且提供了[视频](https://www.youtube.com/playlist?list=PLSE8ODhjZXjYplQRUlrgQKwIAV3es0U6t)

- [《6.830/6.814: Database Systems》](http://db.csail.mit.edu/6.830/)

介绍：麻省理工学院数据库系统的一门核心课程。由数据库[Samuel Madden教授](http://db.csail.mit.edu/madden/)[DB Lab](http://db.csail.mit.edu/)推出的课程。前半部分比较基础的数据库的知识包含关系代数、数据模型、范式、查询优化、事务，后半段主要在讲分布式数据库，讲如何达到数据一致性，也是database比较火的研究方向。

- [《Use and realization of database systems》](https://db.in.tum.de/teaching/ss19/impldb/?lang=en)

介绍：使用并且实现一个数据库系统，这门课程是德国慕尼黑工业大学开设，包含两部分：实现和使用。内容有：事务管理、错误处理、多用户同步、数据的结构、请求处理、分布式数据库、OLTP/OLAP、XML、性能评估。


#### 查询/优化器

- [《How to Architect a Query Compiler, Revisited》](https://www.cs.purdue.edu/homes/rompf/papers/tahboub-sigmod18.pdf)

介绍：本篇论文讲述如何架构一个查询编译器，SQL如何被执行、查询评估、如何处理并行执行、查询器的优化、以及最后的[TPC](http://www.tpc.org/information/benchmarks.asp)测试。

- [《Improved Query Performance with Variant Indexes》](http://ilpubs.stanford.edu:8090/253/1/1997-40.pdf)

介绍：分析型数据库和OLTP数据库需要不同的利弊权衡方式。这反映在索引数据结构的选择上。此文讨论了许多更适合分析型数据库的索引数据结构。

- [《The Case for Learned Index Structures》](https://arxiv.org/abs/1712.01208)

介绍：Google利用深度学习改善索引创建，提交查询效率


#### 事务

- [《Transaction Systems》](https://db.in.tum.de/teaching/ss19/transactions/?lang=en)

介绍：这门课程是德国慕尼黑工业大学开设的关于数据库事务课程。内容有：计算模型、并发控制算法、多版本并发控制、并发控制在对象/查询结构/关系数据库的应用、事务恢复、page恢复算法、如何实现。主要是课件

- [《Generalized Isolation Level Definitions》](http://pmg.csail.mit.edu/papers/icde00.pdf)

介绍：事务隔离是数据库系统设计中根本的组成部分，本文主要从标准层面来讨论隔离级别的划分方式，先解释事务隔离分级的原因以及标准制定的目标；之后概述其发展历史；最后介绍Atul Adya给出的比较合理的隔离级别定义。参考[序列化](http://blog.kongfy.com/2019/03/serializable/)

- [《Percolator: Large-scale Incremental Processing Using Distributed Transactions and Notifications》](https://storage.googleapis.com/pub-tools-public-publication-data/pdf/36726.pdf)    

介绍：Percolator是由Google公司开发的、为大数据集群进行增量处理更新的系统，主要用于google网页搜索索引服务。使用基于Percolator的增量处理系统代替原有的批处理索引系统后，Google在处理同样数据量的文档时，将文档的平均搜索延时降低了50%。[笔记参考](http://andremouche.github.io/transaction/percolator.html)

- [《Improving Optimistic Concurrency Control Through Transaction Batching and Operation Reordering》](http://www.vldb.org/pvldb/vol12/p169-ding.pdf)

介绍：通过事务批量和操作的重排序来提高乐观并发控制性能

- [《Omid: Lock-free transactional support for distributed data stores》]

介绍：Omid一种无锁分布式事务，它是Yahoo公司研发的在大规模分布式存储之上提供事务功能的组件，每隔一段时间都会发布一篇论文。分别是[《Taking Omid to the Clouds》](https://webee.technion.ac.il/~idish/ftp/p842-shacham.pdf)，[《Omid, Reloaded: Scalable and Highly-Available Transaction Processing》](https://www.usenix.org/system/files/conference/fast17/fast17-shacham.pdf)。阅读时推荐和Google发表的Percolator论文一起阅读

- [《Concurrency Control and Recovery in Database Systems》](https://www.microsoft.com/en-us/research/people/philbe/book/)

介绍：经典书籍，讨论数据库的并发控制和恢复。序列化、两阶段锁、MVCC、分布式数据恢复、数据复制

#### 关系模型

- [《Course Introduction and the Relational Model》](https://15445.courses.cs.cmu.edu/fall2019/schedule.html#aug-26-2019)    

介绍：CMU 数据课程，讲述数据库关系模型

#### NewSQL

- [《Spanner: Becoming a SQL System》](https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/46103.pdf)    

介绍：这本论文主要是讲述[Spanner](https://storage.googleapis.com/pub-tools-public-publication-data/pdf/65b514eda12d025585183a641b5a9e096a3c4be5.pdf)的之所以能成功的一些工程经验。如何为一个强大的分布式数据库内核添加SQL支持，如何处理并发问题。其中还列举出了两个案例：分布式中TOPK问题、JOIN随机读问题。

- [《Fast Scans on Key-Value Stores》](http://www.vldb.org/pvldb/vol10/p1526-bocksrocker.pdf)    

介绍：vldb2019年会议论文，如何构建可快速查询的KV存储系统.讲述了KV系统构建时的权衡.该篇是作者博士论文[<Tell: An Elastic Database System for Mixed Workloads>](https://www.systems.ethz.ch/sites/default/files/file/UpcomingPublications/PilmanMarkus2016.pdf)的精简版

- [《Online, Asynchronous Schema Change in F1》](https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/41376.pdf)

介绍：在线异步执行F1 DDL操纵.F1团队提出了一种安全的Schema变更算法。本文将先简单介绍KV存储引擎的提供的接口，然后分析异步的Schema变更导致的问题，最后再描述F1的Schema变更算法以及其限制点。参考阅读[异步 schema 变更](https://github.com/ngaut/builddatabase/blob/master/f1/schema-change.md)。[TiDB 的异步 schema 变更实现](https://github.com/ngaut/builddatabase/blob/master/f1/schema-change-implement.md)


- [《Amazon Aurora: Design Considerations for High Throughput Cloud-Native Relational Databases》](https://www.allthingsdistributed.com/files/p1041-verbitski.pdf)    

介绍：Aurora是一个 OLTP 的关系型数据库。这篇论文描述Aurora架构和设计时的考量。高吞吐的数据处理瓶颈，已经从计算和存储，转移到了网络。Aurora的主要是为了解决多租户scale-out、共享存储、网络瓶颈。[阅读笔记](http://www.zenlife.tk/aurora.md)、[Amazon Aurora: 云原生关系数据库的设计](https://www.allthingsdistributed.com/2019/03/Amazon-Aurora-design-cloud-native-relational-database.html)

- [《Automatically Indexing Millions of Databases in Microsoft Azure SQL Database》](https://www.microsoft.com/en-us/research/uploads/prod/2019/02/autoindexing_azuredb.pdf)    

介绍：vldb2019年会议论文，本文重点讨论了Azure的自动索引推荐系统，讨论了整个过程的细节和反馈。[相关笔记](https://zhuanlan.zhihu.com/p/62628781)

- [《A Lightweight and Efficient Temporal Database Management System in TDSQL》](http://www.vldb.org/pvldb/vol12/p2035-lu.pdf)    

介绍：本文详细讲述了腾讯分布式数据库TDSQL的实现细节和考量

- [《AnalyticDB: Real-time OLAP Database System at Alibaba Cloud》](http://www.vldb.org/pvldb/vol12/p2059-zhan.pdf)    

介绍：AnalyticDB是阿里云构建的OLAP分布式计算数据库，是一种存储和计算分离的架构。在论文中，提到了和阿里基础设施服务盘古和伏羲的结合，并且在此基础上面做的一些工作。论文中有很多大胆的设计，例如所有列都有索引，减少用户的索引维护成本。读写分离，读节点定时拉，写节点主动下推。

#### 学者

- [《Daniel Abadi》](https://www.cs.umd.edu/~abadi/)    

介绍：卡内基梅隆的Daniel Abadi教授，HadoopDB的作者。他的[博客](http://dbmsmusings.blogspot.com/) 质量很高。譬如[讨论事务隔离级别](http://dbmsmusings.blogspot.com/2019/05/introduction-to-transaction-isolation.html)、[2阶段提交](http://dbmsmusings.blogspot.com/2019/01/its-time-to-move-on-from-two-phase.html)

#### 存储

- [《X-Engine: An Optimized Storage Engine for Large-Scale E-Commerce Transaction Processing》](https://dl.acm.org/citation.cfm?id=3314041)    

介绍：这篇论文介绍了阿里云面向大规模流量场景设计的自研存储引擎X-Engine，设计采用分层存储的全新理念，可以根据数据访问频度将数据合理归位，实现快存快取。POLARDB是基于x-engine



#### 其他

- [《Readings in Databases》](https://github.com/rxin/db-readings)

介绍：Apache Spark作者[Reynold Xin](http://twitter.com/rxin)推荐的数据库阅读清单

- [《Awesome Database Learning》](https://github.com/pingcap/awesome-database-learning)

介绍：PingCAP下面的数据库学习资料repository. 