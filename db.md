## 数据库系统(Database System)资料

- [书籍](#书籍)
- [课程](#课程)
- 进程管理
- [查询/优化器](#查询/优化器)
- 存储
- 事务
- 共享组件
- 关系模型
- 分布式数据库
- [NewSQL](#NewSQL)



#### 书籍

- [《Database System Concepts》](https://kakeboksen.td.org.uit.no/Database%20System%20Concepts%206th%20edition.pdf)

介绍：经典书籍，数据库系统概念。数据库领域的殿堂级作品。夯实数据库理论基础，增强数据库技术内功的必备之选。内容涉及很广：表、SQL、关系模型、事务、数据库设计、分布式、存储、索引、查询处理与优化、并发、数据库分析（postgresql,SQL server）。书的难度系数对于刚刚入门的同学可能不太适合，但可以当作"词典”。配套书籍[网站](https://www.db-book.com/).

- [《A First Course in Database Systems》](http://infolab.stanford.edu/~ullman/fcdb.html)

介绍：经典书籍，数据库系统基础教程。讲述关系数据模型、ER图、约束与触发器、SQL、视图。适合入门数据库系统的同学

#### 课程

- [《CMU 15-721 (SPRING 2018) Advanced Database Systems》](https://15721.courses.cs.cmu.edu/spring2018/)

介绍：卡内基梅隆2018年春季高级数据库课程，对现代数据库管理系统内部的全面研究。它将涵盖高性能事务处理系统（OLTP）和大规模分析系统（OLAP）中的组件核心概念和基础知识。它的[阅读列表](https://15721.courses.cs.cmu.edu/spring2018/schedule.html#jan-24-2018)、[课堂笔记](https://15721.courses.cs.cmu.edu/spring2018/notes/)、[课件](https://15721.courses.cs.cmu.edu/spring2018/slides/)都已经开放。并且提供了[视频](https://www.youtube.com/playlist?list=PLSE8ODhjZXjYplQRUlrgQKwIAV3es0U6t)

#### 查询优化器

- [《How to Architect a Query Compiler, Revisited》](https://www.cs.purdue.edu/homes/rompf/papers/tahboub-sigmod18.pdf)

介绍：本篇论文讲述如何架构一个查询编译器，SQL如何被执行、查询评估、如何处理并行执行、查询器的优化、以及最后的[TPC]([http://www.tpc.org/information/benchmarks.asp](http://www.tpc.org/information/benchmarks.asp))测试。

#### NewSQL

- [《Spanner: Becoming a SQL System》](https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/46103.pdf)    

介绍：这本论文主要是讲述[Spanner](https://storage.googleapis.com/pub-tools-public-publication-data/pdf/65b514eda12d025585183a641b5a9e096a3c4be5.pdf)的之所以能成功的一些工程经验。如何为一个强大的分布式数据库内核添加SQL支持，如何处理并发问题。其中还列举出了两个案例：分布式中TOPK问题、JOIN随机读问题。