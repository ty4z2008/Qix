##分布式系统(Distributed System)资料

---
#####希望转载的朋友，你可以不用联系我．但是**一定要保留原文链接**，因为这个项目还在继续也在不定期更新．希望看到文章的朋友能够学到更多．
---

* [《Reconfigurable Distributed Storage for Dynamic Networks》](http://sydney.edu.au/engineering/it/~gramoli/doc/pubs/OPODIS05.pdf)

介绍:这是一篇介绍在动态网络里面实现分布式系统重构的paper.论文的作者(导师)是MIT读博的时候是做分布式系统的研究的,现在在NUS带学生,不仅仅是[分布式系统](http://www.comp.nus.edu.sg/~gilbert/biblio-projects.html#rambo),还有无线网络.如果感兴趣可以去他的主页了解.

* [《Distributed porgramming liboratory》](http://lpd.epfl.ch/site)

介绍:分布式编程实验室,他们发表的很多的[paper](http://lpd.epfl.ch/site/Publications),其中不仅仅是学术研究,还有一些工业界应用的论文.

* [《MIT Theory of Distributed Systems》](http://groups.csail.mit.edu/tds/)

介绍:麻省理工的分布式系统理论主页,作者南希·林奇在2002年证明了[CAP理论](http://zh.wikipedia.org/wiki/CAP%E5%AE%9A%E7%90%86),并且著《分布式算法》一书.

* [《Notes on Distributed Systems for Young Bloods》](http://www.somethingsimilar.com/2013/01/14/notes-on-distributed-systems-for-young-bloods/)

介绍:分布式系统搭建初期的一些建议

* [《Principles of Distributed Computing》](http://dcg.ethz.ch/lectures/podc_allstars/)

介绍:分布式计算原理课程

* [《Google's Globally-Distributed Database》](http://research.google.com/archive/spanner.html)

介绍:Google全球分布式数据介绍,[中文版](http://dblab.xmu.edu.cn/wp-content/uploads/2012/09/20120925_094508_876.pdf)

* [《The Architecture Of Algolia’s Distributed Search Network》](http://highscalability.com/blog/2015/3/9/the-architecture-of-algolias-distributed-search-network.html)

介绍:Algolia的分布式搜索网络的体系架构介绍

* [《Build up a High Availability Distributed Key-Value Store》](https://medium.com/@siddontang/build-up-a-high-availability-distributed-key-value-store-b4e02bc46e9e)

介绍:构建高可用分布式Key-Value存储系统

* [《Distributed Search Engine with Nanomsg and Bond》](https://daniel-j-h.github.io/post/distributed-search-nanomsg-bond/)

介绍:Nanomsg和Bond的分布式搜索引擎

* [《Distributed Processing With MongoDB And Mongothon》](http://tech.gc.com/distributed-processing-with-mongodb-and-mongothon/)

介绍:使用MongoDB和Mongothon进行分布式处理

* [《Salt: Combining ACID and BASE in a Distributed Database》](http://muratbuffalo.blogspot.jp/2015/02/salt-combining-acid-and-base-in.html)

介绍:分布式数据库中把[ACID与BASE](http://www.sigma.me/2011/06/17/database-ACID-and-BASE.html)结合使用.

* [《Makes it easy to understand Paxos for Distributed Systems》](http://paxos.systems/)

介绍:理解的Paxos的分布式系统,[参考阅读:关于Paxos的历史](http://duanple.blog.163.com/blog/static/709717672012112203543166/)

* [《There is No Now Problems with simultaneity in distributed systems》](http://queue.acm.org/detail.cfm?id=2745385)

介绍:There is No Now Problems with simultaneity in distributed systems

* [《Distributed Systems》](http://www0.cs.ucl.ac.uk/staff/ucacwxe/lectures/ds98-99/)

介绍:伦敦大学学院分布式系统课程课件.

* [《Distributed systems for fun and profit》](http://book.mixu.net/distsys/index.html)

介绍:分布式系统电子书籍.

* [《Distributed Systems Spring 2015》](http://www.andrew.cmu.edu/course/95-702/)

介绍:卡内基梅隆大学春季分布式课程主页

* [《Distributed Systems: Concepts and Design (5th Edition)》](https://azmuri.files.wordpress.com/2013/09/george-coulouris-distributed-systems-concepts-and-design-5th-edition.pdf)

介绍: 电子书,分布式系统概念与设计(第五版)

* [《走向分布式》](http://ithelp.ithome.com.tw/profile/share?id=20060041)

介绍:这是一位台湾网友 ccshih 的文字，短短的篇幅介绍了分布式系统的若干要点。[pdf](http://dcaoyuan.github.io/papers/pdfs/Scalability.pdf)

* [《Introduction to Distributed Systems Spring 2013》](http://thu-cmu.cs.tsinghua.edu.cn/curriculum/dscourse/index.htm)

介绍:清华大学分布式系统课程主页,里面的schedule栏目有很多宝贵的资源

* [《Distributed systems》](http://book.mixu.net/distsys/index.html)

介绍:免费的在线分布式系统书籍

* [《Some good resources for learning about distributed computing》](http://www.quora.com/What-are-some-good-resources-for-learning-about-distributed-computing-Why)

介绍:Quora上面的一篇关于学习分布式计算的资源.

* [《Spanner: Google’s Globally-Distributed Database》](http://static.googleusercontent.com/external_content/untrusted_dlcp/research.google.com/es//archive/spanner-osdi2012.pdf)

介绍:这个是第一个全球意义上的分布式数据库，也是Google的作品。其中介绍了很多一致性方面的设计考虑，为了简单的逻辑设计，还采用了原子钟，同样在分布式系统方面具有很强的借鉴意义.

* [《The Chubby lock service for loosely-coupled distributed systems》](http://static.googleusercontent.com/external_content/untrusted_dlcp/research.google.com/zh-CN//archive/chubby-osdi06.pdf)

介绍:Google的统面向松散耦合的分布式系统的锁服务,这篇论文详细介绍了Google的分布式锁实现机制Chubby。Chubby是一个基于文件实现的分布式锁，Google的Bigtable、Mapreduce和Spanner服务都是在这个基础上构建的，所以Chubby实际上是Google分布式事务的基础，具有非常高的参考价值。另外，著名的zookeeper就是基于Chubby的开源实现.推荐[The google stack](http://malteschwarzkopf.de/research/assets/google-stack.pdf),[Youtube:The Chubby lock service for loosely-coupled distributed systems](https://www.youtube.com/watch?v=PqItueBaiRg)

* [《Sinfonia: a new paradigm for building scalable distributed systems》](http://www.sosp2007.org/papers/sosp064-aguilera.pdf)

介绍:这篇论文是SOSP2007的Best Paper，阐述了一种构建分布式文件系统的范式方法，个人感觉非常有用。淘宝在构建TFS、OceanBase和Tair这些系统时都充分参考了这篇论文.

* [《Data-Intensive Text Processing with MapReduce》](http://lintool.github.io/MapReduceAlgorithms/MapReduce-book-final.pdf)

介绍:Ebook:Data-Intensive Text Processing with MapReduce.

* [《Design and Implementation of a Query Processor for a Trusted Distributed Data Base Management System》](http://www.utdallas.edu/~bxt043000/Publications/Journal-Papers/DAS/J16_Design_and_Implementation_of_a_Distributed_Query_Processor.pdf)

介绍:Design and Implementation of a Query Processor for a Trusted Distributed Data Base Management System.

* [《Distributed Query Processing》](http://ogsa-dai.sourceforge.net/documentation/ogsadai4.0/ogsadai4.0-gt/DQPPart.html)

介绍:分布式查询入门.

* [《Distributed Systems and the End of the API》](http://writings.quilt.org/2014/05/12/distributed-systems-and-the-end-of-the-api/)

介绍:分布式系统和api总结.

* [《Distributed Query Reading》](http://www.andrew.cmu.edu/course/15-749/READINGS/required/)

介绍:分布式系统阅读论文，此外还推荐github上面的一个论文列表[The Distributed Reader](http://reiddraper.github.io/distreader/)。

* [《Replication, atomicity and order in distributed systems》](http://afeinberg.github.io/2011/06/17/replication-atomicity-and-order-in-distributed-systems.html)

介绍:Replication, atomicity and order in distributed systems

* [《MIT course:Distributed Systems》](http://nil.csail.mit.edu/6.824/2015/)

介绍:2015年MIT分布式系统课程主页，这次用Golang作为授课语言。[6.824 Distributed Systems](https://pdos.csail.mit.edu/6.824/)课程主页

* [《Distributed systems for fun and profit》](http://book.mixu.net/distsys/)

介绍:免费分布式系统电子书。

* [《Ori：A Secure Distributed File System》](http://ori.scs.stanford.edu/)

介绍:斯坦福开源的分布式文件系统。

* [《Availability in Globally Distributed Storage Systems》](http://static.googleusercontent.com/media/research.google.com/en/us/pubs/archive/36737.pdf)

介绍:Google论文：设计一个高可用的全球分布式存储系统。

* [《Calvin: Fast Distributed Transactions For Partitioned Database Systems》](http://highscalability.com/blog/2013/5/23/paper-calvin-fast-distributed-transactions-for-partitioned-d.html)

介绍:对于分区数据库的分布式事务处理。

* [《Distributed Systems Building Block: Flake Ids》](http://yellerapp.com/posts/2015-02-09-flake-ids.html)

介绍:Distributed Systems Building Block: Flake Ids.

* [《Introduction to Distributed System Design》](http://www.hpcs.cs.tsukuba.ac.jp/~tatebe/lecture/h23/dsys/dsd-tutorial.html)

介绍:Google Code University课程，如何设计一个分布式系统。

* [《Sheepdog: Distributed Storage System for KVM》](http://sheepdog.github.io/sheepdog/)

介绍:KVM的分布式存储系统.

* [《Readings in Distributed Systems Systems》](http://henryr.github.io/distributed-systems-readings/)

介绍:分布式系统课程列表,包括数据库、算法等.

* [《Tera》](https://github.com/BaiduPS/tera)

介绍:来自百度的分布式表格系统.

* [《Distributed systems: for fun and profit》](https://github.com/mixu/distsysbook)

介绍:分布式系统的在线电子书.

* [《Distributed Systems Reading List》](https://github.com/notgary/distributed-systems-reading-list)

介绍:分布式系统资料,此外还推荐[Various articles about distributed systems](https://github.com/hiremaga/readings).

* [《Designs, Lessons and Advice from Building Large Distributed Systems》](http://www.cs.cornell.edu/projects/ladis2009/talks/dean-keynote-ladis2009.pdf)

介绍:Designs, Lessons and Advice from Building Large Distributed Systems.

* [《Testing a Distributed System》](http://queue.acm.org/detail.cfm?ref=rss&id=2800697)

介绍:Testing a distributed system can be trying even under the best of circumstances.

* [《The Google File System》](https://research.google.com/archive/gfs-sosp2003.pdf)

介绍: 基于普通服务器构建超大规模文件系统的典型案例，主要面向大文件和批处理系统， 设计简单而实用。 GFS是google的重要基础设施， 大数据的基石， 也是Hadoop HDFS的参考对象。 主要技术特点包括： 假设硬件故障是常态（容错能力强）， 64MB大块， 单Master设计，Lease/链式复制， 支持追加写不支持随机写.

* [《Bigtable: A Distributed Storage System for Structured Data》](https://research.google.com/archive/bigtable-osdi06.pdf)

介绍:支持PB数据量级的多维非关系型大表， 在google内部应用广泛，大数据的奠基作品之一 ， Hbase就是参考BigTable设计。 Bigtable的主要技术特点包括： 基于GFS实现数据高可靠， 使用非原地更新技术（LSM树）实现数据修改， 通过range分区并实现自动伸缩等.[中文版](http://dblab.xmu.edu.cn/wp-content/uploads/2012/05/20120508_172346_207.pdf)

* [《PacificA: Replication in Log-Based Distributed Storage Systems》](http://research.microsoft.com:8082/pubs/66814/tr-2008-25.pdf)

介绍:面向log-based存储的强一致的主从复制协议， 具有较强实用性。 这篇文章系统地讲述了主从复制系统应该考虑的问题， 能加深对主从强一致复制的理解程度。 技术特点： 支持强一致主从复制协议， 允许多种存储实现， 分布式的故障检测/Lease/集群成员管理方法.

* [《Object Storage on CRAQ, High-throughput chain replication for read-mostly workloads》](http://sns.cs.princeton.edu/docs/craq-usenix09.pdf)

介绍:分布式存储论文:支持强一直的链式复制方法， 支持从多个副本读取数据,实现[code](https://github.com/jterrace/craq).

* [《Finding a needle in Haystack: Facebook’s photo storage》](https://www.usenix.org/legacy/event/osdi10/tech/full_papers/Beaver.pdf)

介绍:Facebook分布式Blob存储,主要用于存储图片. 主要技术特色:小文件合并成大文件,小文件元数据放在内存因此读写只需一次IO.


* [《Windows Azure Storage: A Highly Available Cloud Storage Service with Strong Consistency》](http://www-bcf.usc.edu/~minlanyu/teach/csci599-fall12/papers/11-calder.pdf)

介绍: 微软的分布式存储平台, 除了支持类S3对象存储，还支持表格、队列等数据模型. 主要技术特点：采用Stream/Partition两层设计（类似BigTable）;写错（写满）就封存Extent,使得副本字节一致, 简化了选主和恢复操作; 将S3对象存储、表格、队列、块设备等融入到统一的底层存储架构中.

* [《Paxos Made Live – An Engineering Perspective》](http://www.eecs.harvard.edu/cs262/Readings/paxosmadelive.pdf)

介绍:从工程实现角度说明了Paxo在chubby系统的应用， 是理解Paxo协议及其应用场景的必备论文。 主要技术特点： paxo协议， replicated log， multi-paxo.[参考阅读:关于Paxos的历史](http://duanple.blog.163.com/blog/static/709717672012112203543166/)

* [《Dynamo: Amazon’s Highly Available Key-Value Store》](http://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf)

介绍:Amazon设计的高可用的kv系统,主要技术特点：综和运用一致性哈希,vector clock,最终一致性构建一个高可用的kv系统， 可应用于amazon购物车场景.新内容来自[分布式存储必读论文](http://50vip.com/423.html)

* [《Efficient Replica Maintenance for Distributed Storage Systems》](http://oceanstore.cs.berkeley.edu/publications/papers/pdf/carbonite06.pdf)

介绍:分布式存储系统中的副本存储问题.

* [《PADS: A Policy Architecture for Distributed Storage Systems》](https://www.cs.nyu.edu/rgrimm/papers/nsdi09.pdf)

介绍:分布式存储系统架构.

* [《The Chirp Distributed Filesystem》](http://ccl.cse.nd.edu/software/chirp/)

介绍:开源分布式文件系统Chirp,对于想深入研究的开发者可以阅读文章的相关Papers.

* [《Time, Clocks, and the Ordering of Events in a Distributed System》](http://research.microsoft.com/en-us/um/people/lamport/pubs/time-clocks.pdf)

介绍:经典论文分布式时钟顺序的实现原理.

* [《Making reliable distributed systems in the presence of sodware errors》](http://www.erlang.org/download/armstrong_thesis_2003.pdf)

介绍:面向软件错误构建可靠的分布式系统,[中文笔记](http://www.cnblogs.com/me-sa/archive/2012/05/20/2510564.html).

* [《MapReduce: Simplified Data Processing on Large Clusters》](https://research.google.com/archive/mapreduce-osdi04.pdf)

介绍:MapReduce:超大集群的简单数据处理.

* [《Distributed Computer Systems Engineering》](http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-824-distributed-computer-systems-engineering-spring-2006/index.htm)

介绍:麻省理工的分布式计算课程主页,里面的ppt和阅读列表很多干货.

* [《The Styx Architecture for Distributed Systems》](http://www.vitanuova.com/inferno/papers/styx.html)

介绍:分布式系统Styx的架构剖析.

* [《What are some good resources for learning about distributed computing? Why?》](https://www.quora.com/What-are-some-good-resources-for-learning-about-distributed-computing-Why)

介绍:Quora上面的一个问答:有哪些关于分布式计算学习的好资源.

* [《RebornDB: The Next Generation Distributed Key-Value Store》](http://highscalability.com/blog/2015/7/8/reborndb-the-next-generation-distributed-key-value-store.html)

介绍:下一代分布式k-v存储数据库.

* [《Operating System Concepts Ninth Edition》](http://codex.cs.yale.edu/avi/os-book/OS9/)

介绍:分布式系统归根结底还是需要操作系统的知识,这是耶鲁大学的操作系统概念书籍首页,里面有提供了第8版的在线电子版和最新的学习操作系统指南,学习分布式最好先学习操作系统.

* [《The Log: What every software engineer should know about real-time data's unifying abstraction》](http://engineering.linkedin.com/distributed-systems/log-what-every-software-engineer-should-know-about-real-time-datas-unifying)

介绍:分布式系统Log剖析,非常的详细与精彩. [中文翻译](https://github.com/oldratlee/translations/blob/master/log-what-every-software-engineer-should-know-about-real-time-datas-unifying/README.md) |  [中文版笔记](http://www.cnblogs.com/foreach-break/p/notes_about_distributed_system_and_The_log.html).

* [《Operating Systems Study Guide》](http://faculty.salina.k-state.edu/tim/ossg/index.html)

介绍:分布式系统基础之操作系统学习指南.

* [《分布式系统领域经典论文翻译集》](http://duanple.blog.163.com/blog/static/709717672011330101333271/)

介绍:分布式系统领域经典论文翻译集.

* [《Maintaining performance in distributed systems》](https://speakerdeck.com/elasticsearch/maintaining-performance-in-distributed-systems)

介绍:分布式系统性能维护.

* [《Computer Science from the Bottom Up》](http://www.bottomupcs.com/)

介绍:计算机科学，自底向上,小到机器码,大到操作系统内部体系架构,学习操作系统的另一个在线好材料.

* [《Operating Systems: Three Easy Pieces》](http://pages.cs.wisc.edu/~remzi/OSTEP/)

介绍:<操作系统:三部曲>在线电子书,虚拟、并发、持续.

* [《Database Systems: reading list》](http://www.cs286.net/home/reading-list)

介绍:数据库系统经典论文阅读列,此外推送github上面的[db reading](https://github.com/rxin/db-readings).

* [《Unix System Administration》](http://www.washington.edu/R870/)

介绍:Unix System Administration ebook.

* [《The Amoeba Distributed Operating System》](https://www.cs.vu.nl/~ast/publications/compcom-1991.pdf)

介绍:分布式系统经典论文.

* [《Principles of Computer Systems》](http://web.mit.edu/6.826/archive/S04/)

介绍:计算机系统概念，以分布式为主.此外推荐[Introduction to Operating Systems](http://www2.cs.uregina.ca/~hamilton/courses/330/notes/index.html)笔记

* [《Person page of EMİN GÜN SİRER》](http://www.cs.cornell.edu/People/egs/)

介绍:推荐康奈尔大学的教授EMİN GÜN SİRER的主页,他的研究项目有分布式,数据存储。例如[HyperDex](http://hyperdex.org/papers/)数据库就是他的其中一个项目之一.

* [《Scalable, Secure, and Highly Available Distributed File Access》](http://www.cs.cmu.edu/afs/cs/project/coda-www/ResearchWebPages/docdir/scalable90.pdf)

介绍:来自卡内基梅隆如何构建可扩展的、安全、高可用性的分布式文件系统,[其他papers](http://www.cs.cmu.edu/afs/cs/project/coda-www/ResearchWebPages/docdir/).

* [《Distributed (Deep) Machine Learning Common》](http://dmlc.github.io/)

介绍:分布式机器学习常用库.

* [《The Datacenter as a Computer》](http://www.cs.berkeley.edu/~rxin/db-papers/WarehouseScaleComputing.pdf)

介绍:介绍了如何构建仓储式数据中心,尤其是对于现在的云计算,分布式学习来说很有帮助.本书是[Synthesis Lectures on Computer Architecture](http://www.morganclaypool.com/toc/cac/1/1)系列的书籍之一,这套丛书还有 《The Memory System》,《Automatic Parallelization》,《Computer Architecture Techniques for Power Efficiency》,《Performance Analysis and Tuning for General Purpose Graphics Processing Units》,《Introduction to Reconfigurable Supercomputing》 等

* [《helsinki:Distributed Systems Course slider》](http://www.cs.helsinki.fi/u/jakangas/Teaching/)

介绍:来自芬兰赫尔辛基的分布式系统课程课件:什么是分布式,复制,一致性,容错,同步,通信.

* [《TiDB is a distributed SQL database》](https://github.com/pingcap/tidb)

介绍:分布式数据库TiDB,Golang开发.

* [《S897: Large-Scale Systems》](http://people.csail.mit.edu/matei/courses/2015/6.S897/)

介绍:课程资料:大规模系统.

* [《Large-scale L-BFGS using MapReduce》](http://papers.nips.cc/paper/5333-consistency-of-weighted-majority-votes)

介绍:使用MapReduce进行大规模分布式集群环境下并行L-BFGS.

* [《Twitter是如何构建高性能分布式日志的》](http://www.infoq.com/cn/news/2015/09/BookKeeper-Twitter)

介绍:Twitter是如何构建高性能分布式日志的.

* [《Distributed Systems: When Limping Hardware Is Worse Than Dead Hardware》](http://danluu.com/limplock/)

介绍:在分布式系统中某个组件彻底死了影响很小，但半死不活（网络/磁盘），对整个系统却是毁灭性的.

* [《Tera - 高性能、可伸缩的结构化数据库》](https://github.com/baidu/tera)

介绍:来自百度的分布式数据库.

* [《SequoiaDB is a distributed document-oriented NoSQL Database》](https://github.com/SequoiaDB/SequoiaDB)

介绍:SequoiaDB分布式文档数据库开源.

* [《Readings in distributed systems》](http://henryr.github.io/distributed-systems-readings/)

介绍:这个网址里收集了一堆各TOP大学分布式相关的课程.

* [《Paxos vs Raft》](https://ramcloud.stanford.edu/~ongaro/userstudy/)

介绍:这个网站是[Raft算法](https://raft.github.io/)的作者为教授Paxos和[Raft算法](https://raft.github.io/)做的，其中有两个视频链接，分别讲上述两个算法.[参考阅读:关于Paxos的历史](http://duanple.blog.163.com/blog/static/709717672012112203543166/)

* [《A Scalable Content-Addressable Network》](http://www.eecs.harvard.edu/~mema/courses/cs264/papers/p13-ratnasamy.pdf)

介绍:A Scalable Content-Addressable Network.

* [《500 Lines or Less》](https://github.com/aosabook/500lines)

介绍:这个项目其实是一本书（ [The Architecture of Open Source Applications](http://aosabook.org/en/index.html)）的源代码附录，是一堆大牛合写的.

* [《MIT 6.824 Distributed System》](http://nil.csail.mit.edu/6.824/2015/schedule.html)

介绍:这只是一个课程主页，没有上课的视频，但是并不影响你跟着它上课：每一周读两篇课程指定的论文，读完之后看lecture-notes里对该论文内容的讨论，回答里面的问题来加深理解，最后在课程lab里把所看的论文实现。当你把这门课的作业刷完后，你会发现自己实现了一个分布式数据库.

* [《HDFS-alike in Go》](https://github.com/michaelmaltese/golang-distributed-filesystem)

介绍:使用go开发的分布式文件系统.

* [《What are some good resources for learning about distributed computing? Why?》](https://www.quora.com/What-are-some-good-resources-for-learning-about-distributed-computing-Why)

介绍:Quora上关于学习分布式的资源问答.

* [《SeaweedFS is a simple and highly scalable distributed file system》](https://github.com/chrislusf/seaweedfs)

介绍:SeaweedFS是使用go开发的分布式文件系统项目,代码简单，逻辑清晰.

* [《Codis - yet another fast distributed solution for Redis》](https://github.com/wandoulabs/codis)

介绍:Codis 是一个分布式 Redis 解决方案, 对于上层的应用来说, 连接到 Codis Proxy 和连接原生的 Redis Server 没有明显的区别 

* [《Paper: Coordination Avoidance In Distributed Databases By Peter Bailis》](http://www.bailis.org/papers/bailis-thesis.pdf)

介绍:Coordination Avoidance In Distributed Databases.

* [《从零开始写分布式数据库》](https://github.com/ngaut/builddatabase)

介绍:本文以[TiDB](https://github.com/pingcap/tidb) 源码为例.

* [《what we talk about when we talk about distributed systems》](http://videlalvaro.github.io/2015/12/learning-about-distributed-systems.html)

介绍:分布式系统概念梳理,为分布式系统涉及的主要概念进行了梳理.

* [《Distributed locks with Redis》](http://redis.io/topics/distlock)

介绍:使用Redis实现分布式锁.

* [《CS244b: Distributed Systems》](http://www.scs.stanford.edu/14au-cs244b/)

介绍: 斯坦福2014年秋季分布式课程.

* [《RAMP Made Easy》](http://rustyrazorblade.com/2015/11/ramp-made-easy/)

介绍: 分布式的“读原子性”.

* [《Strategies and Principles of Distributed Machine Learning on Big Data》](http://arxiv.org/abs/1512.09295)

介绍: 大数据分布式机器学习的策略与原理.

* [《Distributed Systems: What is the CAP theorem?》](https://www.quora.com/Distributed-Systems/What-is-the-CAP-theorem)

介绍: 分布式CAP法则.

* [《How should I start to learn distributed storage system as a beginner?》](https://www.quora.com/How-should-I-start-to-learn-distributed-storage-system-as-a-beginner)

介绍: 新手如何步入分布式存储系统.

* [《Cassandra - A Decentralized Structured Storage System》](https://www.cs.cornell.edu/projects/ladis2009/papers/lakshman-ladis2009.pdf)

介绍: 分布式存储系统Cassandra剖析,推荐白皮书[Introduction to Apache Cassandra](http://www.datastax.com/wp-content/uploads/2012/08/WP-IntrotoCassandra.pdf).

* [《What is the best resource to learn about distributed systems?》](https://www.quora.com/What-is-the-best-resource-to-learn-about-distributed-systems)

介绍: 分布式系统学习资源.

* [《What are some high performance TCP hacks?》](https://www.quora.com/What-are-some-high-performance-TCP-hacks)

介绍: 一些高性能TCP黑客技巧.

* [《Maintaining performance in distributed systems》](https://speakerdeck.com/elasticsearch/maintaining-performance-in-distributed-systems)

介绍:分布式系统性能提升.

* [《A simple totally ordered broadcast protocol》](http://diyhpl.us/~bryan/papers2/distributed/distributed-systems/zab.totally-ordered-broadcast-protocol.2008.pdf)

介绍:Benjamin Reed 和 Flavio P.Junqueira 所著论文,对Zab算法进行了介绍,zab算法是Zookeeper保持数据一致性的核心,在国内有很多公司都使用zookeeper做为分布式的解决方案.推荐与此相关的一篇文章[ZooKeeper’s atomic broadcast protocol: Theory and practice](http://www.tcs.hut.fi/Studies/T-79.5001/reports/2012-deSouzaMedeiros.pdf).

* [《zFS - A Scalable Distributed File System Using Object Disk》](http://storageconference.us/2003/papers/29-Rodeh-zFS.pdf)

介绍:可扩展的分布式文件系统ZFS,[The Zettabyte File System](https://users.soe.ucsc.edu/~scott/courses/Fall04/221/zfs_overview.pdf),[End-to-end Data Integrity for File Systems: A ZFS Case Study](http://research.cs.wisc.edu/adsl/Publications/zfs-corruption-fast10.pdf).

* [《A Distributed Haskell for the Modern Web》](http://videlalvaro.github.io/2015/12/learning-about-distributed-systems.html)

介绍:分布式Haskell在当前web中的应用.

* [《Reasoning about Consistency Choices in Distributed Systems》](https://pages.lip6.fr/Marc.Shapiro/papers/CISE-POPL-2016.pdf)

介绍:POPL2016的论文,关于分布式系统一致性选择的论述,[POPL所接受的论文](http://conf.researchr.org/track/POPL-2016/POPL-2016-papers#event-overview),github上已经有人[整理](https://github.com/gasche/popl2016-papers).

* [《Paxos Made Simple》](http://research.microsoft.com/en-us/um/people/lamport/pubs/paxos-simple.pdf)

介绍:Paxos让分布式更简单.[译文](http://dsdoc.net/paxosmadesimple/index.html).[参考阅读:关于Paxos的历史](http://duanple.blog.163.com/blog/static/709717672012112203543166/)

* [《Consensus Protocols: Paxos》](http://the-paper-trail.org/blog/consensus-protocols-paxos/)

介绍:分布式系统一致性协议:Paxos.[参考阅读:关于Paxos的历史](http://duanple.blog.163.com/blog/static/709717672012112203543166/)

* [《Consensus on Transaction Commit》](http://research.microsoft.com/pubs/64636/tr-2003-96.pdf)

介绍：事务提交的一致性探讨.

* [《The Part-Time Parliaments》](http://research.microsoft.com/en-us/um/people/lamport/pubs/lamport-paxos.pdf)

介绍:在《The Part-Time Parliament》中描述了基本协议的交互过程。在基本协议的基础上完善各种问题得到了最终的议会协议。 为了让人更容易理解《The Part-Time Parliament》中描述的Paxos算法，Lamport在2001发表了[《Paxos Made Simple》](http://research.microsoft.com/en-us/um/people/lamport/pubs/paxos-simple.pdf)，以更平直的口头语言描述了Paxos，而没有包含正式的证明和数学术语。[《Paxos Made Simple》](http://research.microsoft.com/en-us/um/people/lamport/pubs/paxos-simple.pdf)中，将算法的参与者更细致的划分成了几个角色：Proposer、Acceptor、Learner。另外还有Leader和Client.[参考阅读:关于Paxos的历史](http://duanple.blog.163.com/blog/static/709717672012112203543166/)

* [《Paxos Made Practical》](https://pdos.csail.mit.edu/archive/6.824-2007/papers/mazieres-paxos.pdf)

介绍:看这篇论文时可以先看看[理解Paxos Made Practical](http://blog.csdn.net/bluecloudmatrix/article/details/41138363).

* [《PaxosLease: Diskless Paxos for Leases》](http://arxiv.org/pdf/1209.4187.pdf)

介绍：PaxosLease：实现租约的无盘Paxos算法,[译文](http://dsdoc.net/paxoslease/index.html).

* [《Paxos Made Moderately Complex》](https://people.csail.mit.edu/matei/courses/2015/6.S897/readings/paxos-moderately-complex.pdf)

介绍：[Paxos算法](http://paxos.systems/)实现,[译文](http://dsdoc.net/paxosmademoderatelycomplex/index.html),同时推荐[42 Paxos Made Moderately Complex](http://www.cs.cornell.edu/courses/cs7412/2011sp/paxos.pdf).

* [《Hadoop Reading List》](http://duanple.blog.163.com/blog/static/7097176720119791920962/)

介绍：Hadoop学习清单.

* [《Hadoop Reading List》](http://duanple.blog.163.com/blog/static/7097176720119791920962/)

介绍：Hadoop学习清单.

* [《2010 NoSQL Summer Reading List》](http://www.empiricalreality.com/2010/09/22/2010-nosql-summer-reading-list/)

介绍：NoSQL知识清单,里面不仅仅包含了数据库阅读清单还包含了分布式系统资料.

* [《Raft: Understandable Distributed Consensus》](http://thesecretlivesofdata.com/raft/)

介绍：Raft可视化图帮助理解分布式一致性

* [《Etcd:Distributed reliable key-value store for the most critical data of a distributed system》](https://github.com/coreos/etcd)

介绍：Etcd分布式Key-Value存储引擎

* [《Understanding Availability》](http://sysnet.ucsd.edu/recall/papers/iptps.pdf)

介绍：理解peer-to-peer系统中的可用性究竟是指什么.同时推荐[基于 Peer-to-Peer 的分布式存储系统的设计](http://www.jos.org.cn/1000-9825/15/268.pdf)

* [《Process structuring, synchronization, and recovery using atomic actions》](http://courses.cs.vt.edu/~cs5204/fall07-kafura/Papers/TransactionalMemory/Lomet.pdf)

介绍：经典论文

* [《Programming Languages for Parallel Processing》](http://www.eng.auburn.edu/files/file1358.pdf)

介绍：并行处理的编程语音

* [《Analysis of Six Distributed File Systems》](https://hal.inria.fr/hal-00789086/file/a_survey_of_dfs.pdf)

介绍：此篇论文对HDFS,MooseFS,iRODS,Ceph,GlusterFS,Lustre六个存储系统做了详细分析.如果是自己研发对应的存储系统推荐先阅读此篇论文

* [《A Survey of Distributed File Systems》](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=A106388C6F04609BCA27DE6DF9C917A6?doi=10.1.1.35.4793&rep=rep1&type=pdf)

介绍：分布式文件系统综述

* [《Concepts of Concurrent Programming》](ftp://ftp.sei.cmu.edu/pub/education/cm24.pdf)

介绍：并行编程的概念,同时推荐[卡内基梅隆FTP](ftp://ftp.sei.cmu.edu/pub/education/)

* [《Concurrency Control Performance Modeling:Alternatives and Implications》](https://www.cs.berkeley.edu/~brewer/cs262/ConcControl.pdf)

介绍：并发控制性能建模：选择与意义

* [《Distributed Systems - Concepts and Design 5th Edition》](https://azmuri.files.wordpress.com/2013/09/george-coulouris-distributed-systems-concepts-and-design-5th-edition.pdf)

介绍：ebook分布式系统概念与设计

* [《分布式系统设计的形式方法》](http://read.pudn.com/downloads51/ebook/174460/03.pdf)

介绍：分布式系统设计的形式方法

* [《互斥和选举算法》](http://read.pudn.com/downloads51/ebook/174460/04.pdf)

介绍：互斥和选举算法

* [《Actors：A model Of Concurrent Cornputation In Distributed Systems》](https://www.cypherpunks.to/erights/history/actors/AITR-844.pdf)

介绍：经典论文

* [《Security Engineering: A Guide to Building Dependable Distributed Systems》](https://www.cl.cam.ac.uk/~rja14/Papers/)

介绍：如何构建一个安全可靠的分布式系统,[About the Author](https://www.cl.cam.ac.uk/~rja14/Papers/SEv2-acks.pdf),[Bibliography:文献资料](https://www.cl.cam.ac.uk/~rja14/Papers/SEv2-biblio.pdf),章节访问把[链接](https://www.cl.cam.ac.uk/~rja14/Papers/SEv2-c01.pdf)最后的01换成01-27即可

* [《15-712 Advanced and Distributed Operating Systems》](https://www.cs.cmu.edu/~15712/index.html)

介绍：卡内基梅隆大学的分布式系统博士生课程主页,有很丰富的[资料](https://www.cs.cmu.edu/~15712/syllabus.html)

* [《Dapper, Google's Large-Scale Distributed Systems Tracing Infrastructure》](http://static.googleusercontent.com/media/research.google.com/zh-CN//archive/papers/dapper-2010-1.pdf)

介绍：Dapper，大规模分布式系统的跟踪系统,[译文](http://bigbully.github.io/Dapper-translation/),[译文对照](http://dirlt.com/dapper.html)

* [《CS262a: Advanced Topics in Computer Systems》](http://www.cs.berkeley.edu/~brewer/cs262/)

介绍：伯克利大学计算机系统进阶课程,内容有深度,涵盖分布式,数据库等内容

* [《Egnyte Architecture: Lessons Learned In Building And Scaling A Multi Petabyte Distributed System》](http://highscalability.com/blog/2016/2/15/egnyte-architecture-lessons-learned-in-building-and-scaling.html)

介绍：PB级分布式系统构建/扩展经验

* [《CS162: Operating Systems and Systems Programming》](https://cs162.eecs.berkeley.edu/)

介绍：伯克利大学计算机系统课程:操作系统与系统编程

* [《MDCC: Multi-Data Center Consistency》](http://mdcc.cs.berkeley.edu/)

介绍：MDCC主要解决跨数据中心的一致性问题中间件,一种新的协议

* [《Research at Google:Distributed Systems and Parallel Computing》](http://research.google.com/pubs/DistributedSystemsandParallelComputing.html)

介绍：google公开对外发表的分布式系统与并行计算论文

* [《HDFS Architecture Guide》](https://hadoop.apache.org/docs/r1.2.1/hdfs_design.html)

介绍：分布式文件系统HDFS架构

* [《ActorDB distributed SQL database》](http://www.actordb.com/index.html)

介绍：分布式 Key/Value数据库

* [《An efficient data location protocol for self-organizing storage clusters》](http://csc.lsu.edu/~gb/csc7700/Reading/SC03_tang.pdf)

介绍：是著名的[Ceph](https://github.com/ceph/ceph)的负载平衡策略，文中提出的几种策略都值得尝试，比较赞的一点是可以对照代码体会和实践,如果你还需要了解可以看看[Ceph:一个 Linux PB 级分布式文件系统](https://www.ibm.com/developerworks/cn/linux/l-ceph/),除此以外,论文的引用部分也挺值得阅读的,同时推荐[Ceph: A Scalable, High-Performance Distributed File System](http://ceph.com/papers/weil-ceph-osdi06.pdf)

* [《A Self-Organizing Storage Cluster for Parallel Data-Intensive Applications》](http://www.supercomputing.org/sc2004/schedule/pdfs/pap283.pdf)

介绍：Surrento的冷热平衡策略就采用了延迟写技术

* [《HBA: Distributed Metadata Management for Large Cluster-Based Storage Systems》](http://www.sersc.org/journals/IJAST/vol36/4.pdf)

介绍：对于分布式存储系统的元数据管理.

* [《Server-Side I/O Coordination for Parallel File Systems》](http://www.mcs.anl.gov/~thakur/papers/sc11-io.pdf)

介绍：服务器端的I/O协调并行文件系统处理,网络,文件存储等都会涉及到IO操作.不过里面涉及到很多技巧性的思路在实践时需要斟酌

* [《Distributed File Systems: Concepts and Examples》](http://www.cs.virginia.edu/~zaher/classes/CS656/levy.pdf)

介绍：分布式文件系统概念与应用

* [《CSE 221: Graduate Operating Systems》](http://cseweb.ucsd.edu/classes/wi08/cse221/)

介绍：加利福尼亚大学的研究生操作系统课程主页，论文很值得阅读

* [《S4: Distributed Stream Computing Platform》](http://cs.brown.edu/~debrabant/cis570-website/papers/s4.pdf)

介绍：Yahoo出品的流式计算系统，目前最流行的两大流式计算系统之一（另一个是storm），Yahoo的主要广告计算平台

* [《Pregel: a system for large-scale graph processing》](https://kowshik.github.io/JPregel/pregel_paper.pdf)

介绍：Google的大规模图计算系统，相当长一段时间是Google PageRank的主要计算系统，对开源的影响也很大（包括GraphLab和GraphChi）

* [《GraphLab: A New Framework for Parallel Machine Learning》](http://www.select.cs.cmu.edu/publications/paperdir/uai2010-low-gonzalez-kyrola-bickson-guestrin-hellerstein.pdf)

介绍：CMU基于图计算的分布式机器学习框架，目前已经成立了专门的商业公司，在分布式机器学习上很有两把刷子，其单机版的GraphChi在百万维度的矩阵分解都只需要2~3分钟；

* [《F1: A Distributed SQL Database That Scales》](http://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/41344.pdf)

介绍：这篇论文是Google 2013年发表的，介绍了F1的架构思路，13年时就开始支撑Google的AdWords业务，另外两篇介绍文章[F1 - The Fault-Tolerant Distributed RDBMS Supporting Google's Ad Business ](http://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/38125.pdf).[Google NewSQL之F1](http://www.leafonsword.org/google-f1/)

* [《Cockroach DB:A Scalable, Survivable, Strongly-Consistent SQL Database》](https://github.com/cockroachdb/cockroach)

介绍：CockroachDB ：一个可伸缩的、跨地域复制的，且支持事务的数据存储,[InfoQ介绍](http://www.infoq.com/cn/news/2014/08/CockroachDB),[Design and Architecture of CockroachDb](https://www.gitbook.com/book/smazumder05/design-and-architecture-of-cockroachdb/details)

* [《Multi-Paxos: An Implementation and Evaluation》](ftp://ftp.cs.washington.edu/tr/2009/09/UW-CSE-09-09-02.PDF)

介绍：Multi-Paxos实现与总结，此外推荐[Paxos/Multi-paxos Algorithm](https://github.com/cocagne/multi-paxos-example),[Multi-Paxos Example](https://github.com/cocagne/multi-paxos-example)，地址:ftp://ftp.cs.washington.edu/tr/2009/09/UW-CSE-09-09-02.PDF

* [《Zab: High-performance broadcast for primary-backup systems》](http://web.stanford.edu/class/cs347/reading/zab.pdf)

介绍：一致性协议zab分析

* [《A Distributed Hash Table》](https://pdos.csail.mit.edu/papers/fdabek-phd-thesis.pdf)

介绍：分布式哈希算法论文,扩展阅读[Introduction to Distributed Hash Tables](https://www.ietf.org/proceedings/65/slides/plenaryt-2.pdf),[Distributed Hash Tables](https://www.cs.cmu.edu/~dga/15-744/S07/lectures/16-dht.pdf)

* [《Comparing the performance of distributed hash tables under churn》](http://www.news.cs.nyu.edu/~jinyang/pub/iptps04.pdf)

介绍：分布式hash表性能的Churn问题

* [《Brewer’s Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web》](https://www.comp.nus.edu.sg/~gilbert/pubs/BrewersConjecture-SigAct.pdf)

介绍：分布式系统的CAP问题,推荐[Perspectives on the CAP Theorem](https://groups.csail.mit.edu/tds/papers/Gilbert/Brewer2.pdf).对CAP理论的解析文章,[PODC ppt](http://www.cs.berkeley.edu/~brewer/cs262b-2004/PODC-keynote.pdf),[A plain english introduction to CAP Theorem](http://ksat.me/a-plain-english-introduction-to-cap-theorem/),[IEEE Computer issue on the CAP Theorem](http://dbmsmusings.blogspot.kr/2012/10/ieee-computer-issue-on-cap-theorem.html)

* [《F2FS: A New File System for Flash Storage》](https://www.usenix.org/system/files/conference/fast15/fast15-paper-lee.pdf)

介绍：闪存存储文件系统F2FS

* [《Better I/O Through Byte-Addressable, Persistent Memory》](http://research.microsoft.com/pubs/81175/BPFS.pdf)

介绍：微软发表的关于i/o访问优化论文

* [《tmpfs: A Virtual Memory File System》](http://www.solarisinternals.com/si/reading/tmpfs.pdf)

介绍：虚拟内存文件系统tmpfs

* [《BTRFS: The Linux B-tree Filesystem》](http://domino.research.ibm.com/library/cyberdig.nsf/papers/6E1C5B6A1B6EDD9885257A38006B6130/$File/rj10501.pdf)

介绍：Linux B-tree文件系统.

* [《Akamai technical publication》](https://www.akamai.com/us/en/our-thinking/technical-publications.jsp)

介绍：Akamai是全球最大的云计算机平台之一，承载了全球15-30%网络流量,如果你是做CDN或者是云服务,这个里面的论文会给你很有帮助.例如这几天看facebook开源的[osquery](https://osquery.io/)。找到通过db的方式运维,找到[Keeping Track of 70,000+ Servers: The Akamai Query System](https://www.akamai.com/es/es/multimedia/documents/technical-publication/keeping-track-of-70000-servers-the-akamai-query-system-technical-publication.pdf)这篇论文，先看论文领会思想，然后再使用工具osquery实践

* [《BASE: An Acid Alternative》](http://dl.acm.org/citation.cfm?id=1394128)

介绍：来自eBay 的解决方案,译文[Base: 一种Acid的替代方案](http://article.yeeyan.org/view/167444/125572),应用案例参考[保证分布式系统数据一致性的6种方案](https://mp.weixin.qq.com/s?__biz=MzAwMDU1MTE1OQ==&mid=2653546976&idx=1&sn=c3fb2338389a41e7ab998c0c21bd3e5d)

* [《A Note on Distributed Computing》](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=CF3CA7E7B62091EB266A1543A6F2D26A?doi=10.1.1.41.7628&rep=rep1&type=pdf)

介绍：Jim Waldo和Sam Kendall等人共同撰写了一篇非常有名的论文“分布式计算备忘录”，这篇论文在Reddit上被人推荐为“每个程序员都应当至少读上两篇”的论文。在这篇论文中，作者表示“忽略本地计算与分布式计算之间的区别是一种危险的思想”，特别指出了Emerald、Argus、DCOM以及CORBA的设计问题。作者将这些设计问题归纳为“三个错误的原则”： “对于某个应用来说，无论它的部署环境如何，总有一种单一的、自然的面向对象设计可以符合其需求。” “故障与性能问题与某个应用的组件实现直接相关，在最初的设计中无需考虑这些问题。” “对象的接口与使用对象的上下文无关”.

* [《Distributed Systems Papers》](https://github.com/papers-we-love/papers-we-love/tree/master/distributed_systems)

介绍：分布式系统领域经典论文列表.

* [《Consistent Hashing and Random Trees: Distributed Caching Protocols for Relieving Hot Spots on the World Wide Web》](https://www.akamai.com/es/es/multimedia/documents/technical-publication/consistent-hashing-and-random-trees-distributed-caching-protocols-for-relieving-hot-spots-on-the-world-wide-web-technical-publication.pdf)

介绍：Consistent Hashing算法描述.

* [《SIGMOD 2016: Accepted Research Papers》](http://sigmod2016.org/pods_list.shtml)

介绍：SIGMOD是世界上最有名的数据库会议之一,最具有权威性,收录论文审核非常严格.2016年的SIGMOD 会议照常进行,上面收录了今年SIGMOD收录的论文,把题目输入google中加上pdf就能找到,很多论文值得阅读,[SIGMOD 2015](http://sigmod2015.org/pods_list.shtml)

* [《Notes on CPSC 465/565: Theory of Distributed Systems》](http://www.cs.yale.edu/homes/aspnes/classes/465/notes.pdf)

介绍:耶鲁大学的分布式系统理论课程笔记

* [《Distributed Operating System Doc PDF》](http://listpdf.com/di/distributed-operating-system-doc-pdf.html)

介绍:分布式系统文档资源（可下载）

* [《Anatomy of a database system》](https://mitpress.mit.edu/sites/default/files/titles/content/9780262693141_sch_0002.pdf)

介绍:数据库系统剖析，这本书是由伯克利大学的[Joseph M. Hellerstein](http://db.cs.berkeley.edu/jmh/)和M. Stonebraker合著的一篇论文.对数据库剖析很有深度.除此以外还有一篇文章[Architecture of a Database System](http://db.cs.berkeley.edu/papers/fntdb07-architecture.pdf)。数据库系统架构,厦门大学的数据库实验室教授林子雨组织过[翻译](http://dblab.xmu.edu.cn/sites/default/files/files/linziyu-Architecture%20of%20a%20Database%20System(Chinese%20Version)-ALL.pdf)

* [《A Relational Model of Data for Large Shared Data Banks》](https://www.seas.upenn.edu/~zives/03f/cis550/codd.pdf)

介绍:数据库关系模型论文

* [《RUC Innovative data systems reaserch lab recommand papers》](http://idke.ruc.edu.cn/reading/index.htm)

介绍:中国人民大学数据研究实验室推荐的数据库领域论文

* [《A Scalable Distributed Information Management System》](http://www.cs.utexas.edu/~dahlin/projects/sdims/papers/sdims-sigcomm.pdf)

介绍:构建可扩展的分布式信息管理系统
