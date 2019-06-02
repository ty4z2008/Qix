## 数据库系统(Database System)资料

- [书籍](#书籍)
- [课程](#课程)
- 进程管理
- [查询/优化器](#查询/优化器)
- 存储
- [事务](#事务)
- 共享组件
- 关系模型
- 分布式数据库
- [NewSQL](#NewSQL)
- [学者](#学者)



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

介绍：本篇论文讲述如何架构一个查询编译器，SQL如何被执行、查询评估、如何处理并行执行、查询器的优化、以及最后的[TPC]([http://www.tpc.org/information/benchmarks.asp](http://www.tpc.org/information/benchmarks.asp))测试。

#### 事务

- [《Transaction Systems》](https://db.in.tum.de/teaching/ss19/transactions/?lang=en)

介绍：这门课程是德国慕尼黑工业大学开设的关于数据库事务课程。内容有：计算模型、并发控制算法、多版本并发控制、并发控制在对象/查询结构/关系数据库的应用、事务恢复、page恢复算法、如何实现。主要是课件

#### NewSQL

- [《Spanner: Becoming a SQL System》](https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/46103.pdf)    

介绍：这本论文主要是讲述[Spanner](https://storage.googleapis.com/pub-tools-public-publication-data/pdf/65b514eda12d025585183a641b5a9e096a3c4be5.pdf)的之所以能成功的一些工程经验。如何为一个强大的分布式数据库内核添加SQL支持，如何处理并发问题。其中还列举出了两个案例：分布式中TOPK问题、JOIN随机读问题。

#### 学者

- [《Daniel Abadi》](https://www.cs.umd.edu/~abadi/)    

介绍：卡内基梅隆的Daniel Abadi教授，HadoopDB的作者。他的[博客](http://dbmsmusings.blogspot.com/) 质量很高。譬如[讨论事务隔离级别](http://dbmsmusings.blogspot.com/2019/05/introduction-to-transaction-isolation.html)、[2阶段提交](http://dbmsmusings.blogspot.com/2019/01/its-time-to-move-on-from-two-phase.html)