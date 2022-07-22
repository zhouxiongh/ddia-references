Designing Data-Intensive Applications
=====================================

Chapter 5 Replication
--------------------

1. Bruce G. Lindsay, Patricia Griffiths Selinger, C. Galtieri, et al.:
    “[Notes on Distributed Databases](http://domino.research.ibm.com/library/cyberdig.nsf/papers/A776EC17FC2FCE73852579F100578964/$File/RJ2571.pdf),” IBM Research, Research Report RJ2571(33471), July 1979.

    > ……因为网络的基本约束条件没有发生本质的改变，可以说自 1970 年所研究的基本复制原则，时至今日也没有发生太大的变化

1. “[Oracle Active Data Guard Real-Time Data Protection and Availability](http://www.oracle.com/technetwork/database/availability/active-data-guard-wp-12c-1896127.pdf),” Oracle White Paper, June 2013.

1. “[AlwaysOn Availability Groups](http://msdn.microsoft.com/en-us/library/hh510230.aspx),” in *SQL Server Books Online*, Microsoft, 2012.

1. Lin Qiao, Kapil Surlaker, Shirshanka Das, et al.:
    “[On Brewing Fresh Espresso: LinkedIn’s Distributed Data Serving Platform](http://www.slideshare.net/amywtang/espresso-20952131),” at *ACM International Conference on
    Management of Data* (SIGMOD), June 2013.

1. Jun Rao:
    “[Intra-Cluster Replication for Apache Kafka](http://www.slideshare.net/junrao/kafka-replication-apachecon2013),” at *ApacheCon North America*, February 2013.

1. “[Highly Available Queues](https://www.rabbitmq.com/ha.html),” in *RabbitMQ Server Documentation*, Pivotal Software, Inc., 2014.

    > 主从复制
    >
    > ……许多关系型数据库都内置支持主从复制，例如postgreSQL、MySQL、oracle Data Guard[2]和 SQL server 的 AlwaysOn Availability Groups[3]。而一些非关系数据库如 mongoDB、RethinkDB 和 Espresso[4] 也支持主从复制。另外，主从复制技术不仅限于数据库，还广泛用于分布式消息队列如 Kafka[5] 和 RabbitMQ[6]，以及一些网络文件系统和复制块设备

1. Yoshinori Matsunobu:
    “[Semi-Synchronous Replication at Facebook](http://yoshinorimatsunobu.blogspot.co.uk/2014/04/semi-synchronous-replication-at-facebook.html),” *yoshinorimatsunobu.blogspot.co.uk*, April 1, 2014.

    > 主从复制
    >
    > ……这种配置有时也称为半同步

1. Robbert van Renesse and Fred B. Schneider:
    “[Chain Replication for Supporting High Throughput and Availability](http://static.usenix.org/legacy/events/osdi04/tech/full_papers/renesse/renesse.pdf),” at *6th USENIX Symposium on
    Operating System Design and Implementation* (OSDI), December 2004.

1. Jeff Terrace and Michael J. Freedman:
    “[Object Storage on CRAQ: High-Throughput Chain Replication for Read-Mostly Workloads](https://www.usenix.org/legacy/event/usenix09/tech/full_papers/terrace/terrace.pdf),” at *USENIX
    Annual Technical Conference* (ATC), June 2009.

1. Brad Calder, Ju Wang, Aaron Ogus, et al.:
    “[Windows Azure Storage: A Highly Available Cloud Storage Service with Strong Consistency](http://sigops.org/sosp/sosp11/current/2011-Cascais/printable/11-calder.pdf),” at *23rd ACM
    Symposium on Operating Systems Principles* (SOSP), October 2011.

1. Andrew Wang:
     “[Windows Azure Storage](https://www.umbrant.com/2016/02/04/windows-azure-storage/),”
     *umbrant.com*, February 4, 2016.

     > 主从复制
     >
     > ……例如，链式复制[8，9]是同步复制的一种变体，以及在一些系统（如 MS Azure 存储[10，11]）中得以实现

1. “[Percona    Xtrabackup - Documentation](https://www.percona.com/doc/percona-xtrabackup/2.1/index.html),” Percona LLC, 2014.

     > 配置新的从节点
     >
     > ……而在某些情况下，可能需要第三方工具，如 MySQL 的 innobackupex

1. Jesse Newland:
      “[GitHub Availability This   Week](https://github.com/blog/1261-github-availability-this-week),” *github.com*, September 14, 2012.

      > 处理节点失效
      >
      > ……例如，在 GitHub 的一个事故，某个数据并非完全同步的 MySQL 从节点被提升为主副本，数据库使用了自增计数器将主键分配给新创建的行，但是因为新的主节点计算器落后于原主节点……最后导致了某些私有数据被错误地泄露给了其他用户

1. Mark Imbriaco:
      “[Downtime Last Saturday](https://github.com/blog/1364-downtime-last-saturday),”
      *github.com*, December 26, 2012.

      > 处理节点失效
      >
      > ……然哦，如果设计或者实现考虑不周，可能会出现两个节点都被关闭的情况

1. John Hugg:
     “[‘All in’ with Determinism for Performance and Testing in Distributed Systems](https://www.youtube.com/watch?v=gJRj3vJL4wE),” at *Strange Loop*, September 2015.

     > 复制日志的实现
     >
     > ……VoltDB 使用基于语句的复制，它通过事务级别的确定性来保证复制的安全

1. Amit Kapila:
     “[WAL Internals of PostgreSQL](http://www.pgcon.org/2012/schedule/attachments/258_212_Internals%20Of%20PostgreSQL%20Wal.pdf),” at *PostgreSQL Conference* (PGCon), May 2012.

     > 基于预写日志传输
     >
     > ……postgreSQL、oracle 以及其他系统等支持这种复制方式

1. [*MySQL Internals Manual*](http://dev.mysql.com/doc/internals/en/index.html).
     Oracle, 2014.

     > 基于行的逻辑日志复制
     >
     > ……MySQL 的二进制日志 binlog 使用该方式

1. Yogeshwer Sharma, Philippe Ajoux, Petchean Ang, et al.:
     “[Wormhole: Reliable Pub-Sub to Support Geo-Replicated Internet Services](https://www.usenix.org/system/files/conference/nsdi15/nsdi15-paper-sharma.pdf),” at *12th USENIX
     Symposium on Networked Systems Design and Implementation* (NSDI), May 2015.

     > 基于行的逻辑日志复制
     >
     > ……如果要将数据库的内容发送到外部系统，或构建自定义索引和缓存等，基于逻辑日志的复制更有优势

1. “[Oracle GoldenGate 12c: Real-Time Access to Real-Time Information](http://www.oracle.com/us/products/middleware/data-integration/oracle-goldengate-realtime-access-2031152.pdf),” Oracle White Paper, October 2013.

     > 基于触发器的复制
     >
     > ……例如 Oracle GoldenGate，可以通过读取数据库日志让应用程序获取数据变更

1. Shirshanka Das, Chavdar Botev, Kapil Surlaker, et al.:
     “[All Aboard the Databus!](http://www.socc2012.org/s18-das.pdf),” at
     *ACM Symposium on Cloud Computing* (SoCC), October 2012.

     > 基于触发器的复制
     >
     > ……Databus 和 Postgres 的 Bucardo 就是这种技术的典型代表

1. Greg Sabino Mullane:
     “[Version 5 of Bucardo Database Replication System](http://blog.endpoint.com/2014/06/bucardo-5-multimaster-postgres-released.html),” *blog.endpoint.com*, June 23, 2014.

1. Werner Vogels:
     “[Eventually Consistent](http://queue.acm.org/detail.cfm?id=1466448),”
     *ACM Queue*, volume 6, number 6, pages 14–19, October 2008.
     [doi:10.1145/1466443.1466448](http://dx.doi.org/10.1145/1466443.1466448)

1. Douglas B. Terry:
     “[Replicated Data Consistency Explained Through Baseball](https://www.microsoft.com/en-us/research/publication/replicated-data-consistency-explained-through-baseball/),” Microsoft Research, Technical Report
     MSR-TR-2011-137, October 2011.

     > 复制滞后问题
     >
     > ……这种不一致只是一个暂时的状态，如果停止写数据库，经过一段时间之后，从节点最终会赶上并于主节点保持一致。这种效应也被称为最终一致性[22，23]
     >
     > ……前缀一致读

1. Douglas B. Terry, Alan J. Demers, Karin Petersen, et al.:
     “[Session Guarantees for Weakly Consistent Replicated Data](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.71.2269&rep=rep1&type=pdf),” at *3rd International Conference
     on Parallel and Distributed Information Systems* (PDIS), September 1994.
     [doi:10.1109/PDIS.1994.331722](http://dx.doi.org/10.1109/PDIS.1994.331722)

     > 读自己的写
     >
     > ……对于这种情况，我们需要“写后读一致性”，也称为读写一致性

1. Terry Pratchett: *Reaper Man: A Discworld
     Novel*. Victor Gollancz, 1991. ISBN: 978-0-575-04979-6

     > 前缀一致读
     >
     > ……首先，这种超自然的力量确认令人印象深刻，但逻辑上却是混乱的

1. “[Tungsten Replicator](https://github.com/holys/tungsten-replicator),” *github.com*.

1. “[BDR 0.10.0 Documentation](http://bdr-project.org/docs/next/index.html),” The PostgreSQL Global Development Group, *bdr-project.org*, 2015.

     > 多主节点复制
     >
     > ……有些数据内嵌支持了多主复制，但有些则借助外部工具来实现，例如 MySQL 的 Tubgsten Replicator[26]，PostgreSQL 的 BDR[27]以及 Oracle 的 GoldenGate[19]

1. Robert Hodges:
     “[If You *Must* Deploy Multi-Master Replication, Read This First](http://scale-out-blog.blogspot.co.uk/2012/04/if-you-must-deploy-multi-master.html),” *scale-out-blog.blogspot.co.uk*,
     March 30, 2012.

     > 多主节点复制
     >
     > ……一些人认为多主复制比较危险，应该谨慎使用或者避免使用

1. J. Chris Anderson, Jan Lehnardt, and Noah
     Slater: *CouchDB: The Definitive Guide*. O'Reilly Media, 2010.
     ISBN: 978-0-596-15589-6

     > 离线客户端操作
     >
     > ……有一些工具可以使多主配置更为容易，如 CouchDB 就是为这种操作模式而设计的

1. AppJet, Inc.:
     “[Etherpad and EasySync Technical Manual](https://github.com/ether/etherpad-lite/blob/e2ce9dc/doc/easysync/easysync-full-description.pdf),” *github.com*, March 26, 2011.

1. John Day-Richter:
     “[What’s Different About the New Google Docs: Making Collaboration Fast](https://drive.googleblog.com/2010/09/whats-different-about-new-google-docs.html),”
     *drive.googleblog.com*, September 23, 2010.

     > 协作编辑
     >
     > ……例如，Etherpad 和 Google Docs 允许多人同时编辑文本文档或电子表格

1. Martin Kleppmann and Alastair R. Beresford:
     “[A Conflict-Free Replicated JSON Datatype](http://arxiv.org/abs/1608.03960),”
     arXiv:1608.03960, August 13, 2016.

     > 协作编辑
     >
     > ……然而另一方面，也会面临所有多主复制都存在的挑战，即如何解决冲突

1. Frazer Clement:
     “[Eventual Consistency – Detecting Conflicts](http://messagepassing.blogspot.co.uk/2011/10/eventual-consistency-detecting.html),” *messagepassing.blogspot.co.uk*, October 20, 2011.

     > 处理写冲突
     >
     > ……但是，当更改被异步复制到对方时，却发现存在冲突

1. Robert Hodges:
     “[State of the Art for MySQL Multi-Master Replication](https://web.archive.org/web/20161010052017/https://www.percona.com/live/mysql-conference-2013/sites/default/files/slides/mysql-multi-master-state-of-art-2013-04-24_0.pdf),” at *Percona Live: MySQL Conference &
     Expo*, April 2013.

     > 避免冲突
     >
     > ……因此，避免冲突反而成为大家普遍推荐的首选方案

1. John Daily:
     “[Clocks Are Bad, or, Welcome to the Wonderful World of Distributed Systems](https://riak.com/clocks-are-bad-or-welcome-to-distributed-systems/),” *riak.com*, November 12, 2013.

     > 收敛于一致状态
     >
     > ……虽然很流行，但是很容易造成数据丢失

1. Riley Berton:
     “[Is Bi-Directional Replication (BDR) in Postgres Transactional?](http://sdf.org/~riley/blog/2016/01/04/is-bi-directional-replication-bdr-in-postgres-transactional/),” *sdf.org*, January 4, 2016.

     > 自定义冲突解决逻辑
     >
     > ……注意，冲突解决通常用于单个行或文档，而不是整个事务

1. Giuseppe DeCandia, Deniz Hastorun, Madan Jampani, et al.:
     “[Dynamo: Amazon's Highly Available Key-Value Store](http://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf),” at *21st ACM Symposium on Operating
     Systems Principles* (SOSP), October 2007.

     > 自动冲突解决
     >
     > ……亚马逊购物车的反面例子

1. Marc Shapiro, Nuno Preguiça, Carlos Baquero,
      and Marek Zawirski: “[A Comprehensive Study of   Convergent and Commutative Replicated Data Types](http://hal.inria.fr/inria-00555588/),” INRIA Research Report no. 7506,
      January 2011.

      > 自动冲突解决
      >
      > ……无冲突的复制数据类型（CRDT）

1. Sam Elliott:
      “[CRDTs: An UPDATE (or   Maybe Just a PUT)](https://speakerdeck.com/lenary/crdts-an-update-or-just-a-put),” at *RICON West*, October 2013.

1. Russell Brown:
      “[A Bluffers Guide to CRDTs in   Riak](https://gist.github.com/russelldb/f92f44bdfb619e089a4d),” *gist.github.com*, October 28, 2013.

      > 自动冲突解决
      >
      > ……一些 CRDT 已经在 Riak2.0 中得以具体实现

1. Benjamin Farinier, Thomas Gazagnaire, and
      Anil Madhavapeddy: “[Mergeable Persistent Data   Structures](http://gazagnaire.org/pub/FGM15.pdf),” at *26es Journées Francophones des Langages Applicatifs* (JFLA),
      January 2015.

      > 自动冲突解决
      >
      > ……可合并的持久数据结构

1. Chengzheng Sun and Clarence Ellis:
      “[Operational   Transformation in Real-Time Group Editors: Issues, Algorithms, and Achievements](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.53.933&rep=rep1&type=pdf),” at
      *ACM Conference on Computer Supported Cooperative Work* (CSCW), November 1998.

      > 自动冲突解决
      >
      > ……操作转换（Operational transformation）

1. Lars Hofhansl:
     “[HBASE-7709: Infinite Loop Possible in Master/Master Replication](https://issues.apache.org/jira/browse/HBASE-7709),” *issues.apache.org*, January 29, 2013.

     > 拓扑结构
     >
     > ……为防止无限循环，每个节点需要赋予一个唯一的标识符，在复制日志中的每个写请求都标记了已通过的节点标识符

1. David K. Gifford:
     “[Weighted Voting for Replicated Data](https://www.cs.cmu.edu/~15-749/READINGS/required/availability/gifford79.pdf),”
     at *7th ACM Symposium on Operating Systems Principles* (SOSP), December 1979.
     [doi:10.1145/800215.806583](http://dx.doi.org/10.1145/800215.806583)

     > 无主节点复制
     >
     > ……其实最早的数据复制系统就是无主节点的（或称为去中心复制，无中心复制），但后来到了关系数据库主导的时代，这个想法被大家选择性遗忘了

1. Heidi Howard, Dahlia Malkhi, and Alexander Spiegelman:
     “[Flexible Paxos: Quorum Intersection Revisited](https://arxiv.org/abs/1608.06696),”
     *arXiv:1608.06696*, August 24, 2016.

     > Quorum 一致性的局限性
     >
     > ……设定其他的 quorum 分配书也是可行的

1. Joseph Blomstedt:
      “[Re: Absolute Consistency](https://web.archive.org/web/20190919171316/http://lists.basho.com:80/pipermail/riak-users_lists.basho.com/2012-January/007157.html),” email to *riak-users* mailing list, *lists.basho.com*,
      January 11, 2012.

      > Quorum 一致性的局限性
      >
      > …… 写操作的 w 节点和读取的 r 节点可能完全不同，因此无法保证读写请求一定存在重叠的节点

1. Joseph Blomstedt:
      “[Bringing Consistency to Riak](https://vimeo.com/51973001),” at *RICON West*,
      October 2012.

      > Quorum 一致性的局限性
      >
      > ……这意味着这样的写操作被视为失败，后续的读操作仍可能返回新值

1. Peter Bailis, Shivaram Venkataraman,
     Michael J. Franklin, et al.:
     “[Quantifying Eventual Consistency with PBS](http://www.bailis.org/papers/pbs-cacm2014.pdf),”
     *Communications of the ACM*, volume 57, number 8, pages 93–102, August 2014.
     [doi:10.1145/2632792](http://dx.doi.org/10.1145/2632792)

     > 监控旧值
     >
     > ……目前针对无主节点复制系统已经有一些研究，根据参数 n，w 和 r 来预测读到旧值的期望百分比

1. Jonathan Ellis:
     “[Modern Hinted Handoff](http://www.datastax.com/dev/blog/modern-hinted-handoff),”
     *datastax.com*, December 11, 2012.

1. “[Project Voldemort Wiki](https://github.com/voldemort/voldemort/wiki),” *github.com*, 2013.

     > 宽松的quorum
     >
     > ……在 Riak 中，默认启用，而在 Cassandra 和 Voldemort 则默认关闭

1. “[Apache Cassandra Documentation](https://cassandra.apache.org/doc/latest/),” Apache Software Foundation, *cassandra.apache.org*.

     > 多数据中心操作
     >
     > 尽管可以灵活配置，但对远程数据中心的写入由于延迟很高，通常都被配置为异步方式[50，51]

1. “[Riak Enterprise: Multi-Datacenter Replication](https://web.archive.org/web/20150513041837/http://basho.com/assets/MultiDatacenter_Replication.pdf).”
     Technical whitepaper, Basho Technologies, Inc., September 2014.

     > 多数据中心操作
     >
     > ……集群之间跨数据中心的复制则在后台异步运行，类似于多主节点复制风格

1. Jonathan Ellis:
     “[Why Cassandra Doesn't Need Vector Clocks](http://www.datastax.com/dev/blog/why-cassandra-doesnt-need-vector-clocks),” *datastax.com*, September 2, 2013.

     > 最后写入者胜
     >
     > ……这个冲突解决算法被称为最后写入者获胜，它是 Cassandra 仅有的冲突解决方法，而在 Riak 中，它是可选方案之一
     >
     > ……例如，Cassandra 的一个推荐使用方法就是采用 UUID 作为主键，这样每个写操作都针对不同的、系统唯一的主键

1. Leslie Lamport:
     “[Time, Clocks, and the Ordering of Events in a Distributed System](https://www.microsoft.com/en-us/research/publication/time-clocks-ordering-events-distributed-system/),” *Communications of the ACM*,
     volume 21, number 7, pages 558–565, July 1978.
     [doi:10.1145/359545.359563](http://dx.doi.org/10.1145/359545.359563)

     > Happens-before 关系和并发
     >
     > ……事实上，我们也可以简单地说，如果两个操作都不再另一个之前发生，那么操作是并发的

1. Joel Jacobson:
     “[Riak 2.0: Data Types](http://blog.joeljacobson.com/riak-2-0-data-types/),”
     *blog.joeljacobson.com*, March 23, 2014.

     > 合并同时写入的值
     >
     > ……例如，Riak 支持称为 CRDT 一系列数据结构

1. D. Stott Parker Jr., Gerald J. Popek, Gerard Rudisin, et al.:
     “[Detection of Mutual Inconsistency in Distributed Systems](http://zoo.cs.yale.edu/classes/cs426/2013/bib/parker83detection.pdf),” *IEEE Transactions on Software Engineering*,
     volume 9, number 3, pages 240–247, May 1983.
     [doi:10.1109/TSE.1983.236733](http://dx.doi.org/10.1109/TSE.1983.236733)

     > 版本矢量
     >
     > ……所有副本的版本号集合称为版本矢量

1. Nuno Preguiça, Carlos Baquero, Paulo Sérgio
     Almeida, et al.: “[Dotted Version Vectors: Logical Clocks for Optimistic Replication](http://arxiv.org/pdf/1011.5808v1.pdf),” arXiv:1011.5808, November 26,
     2010.

1. Sean Cribbs:
     “[A Brief History of Time in Riak](https://speakerdeck.com/seancribbs/a-brief-history-of-time-in-riak),”
     at *RICON*, October 2014.

1. Russell Brown:
     “[Vector Clocks Revisited Part 2: Dotted Version Vectors](https://riak.com/posts/technical/vector-clocks-revisited-part-2-dotted-version-vectors/),” *basho.com*, November 10, 2015.

     > 但最有趣的可能是在 Riak 2.0[58,59] 中使用的虚线版本矢量

1. Carlos Baquero:
     “[Version Vectors Are Not Vector Clocks](https://haslab.wordpress.com/2011/07/08/version-vectors-are-not-vector-clocks/),” *haslab.wordpress.com*, July 8, 2011.

1. Reinhard Schwarz and Friedemann Mattern:
     “[Detecting Causal Relationships in Distributed Computations: In Search of the Holy Grail](http://dcg.ethz.ch/lectures/hs08/seminar/papers/mattern4.pdf),” *Distributed
     Computing*, volume 7, number 3, pages 149–174, March 1994.
     [doi:10.1007/BF02277859](http://dx.doi.org/10.1007/BF02277859)

     > 版本矢量
     >
     > ……版本矢量有时也被称为矢量时钟，然而两者并不完全相同，细微差别可参阅文献[60，61]
