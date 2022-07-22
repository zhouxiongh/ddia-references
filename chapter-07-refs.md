# Designing Data-Intensive Applications

Chapter 7 Transactions
--------------------

1. Donald D. Chamberlin, Morton M. Astrahan, Michael W. Blasgen, et al.:
    “[A History and Evaluation of System R](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.84.348&rep=rep1&type=pdf),” *Communications of the ACM*,
    volume 24, number 10, pages 632–646, October 1981.
    [doi:10.1145/358769.358784](http://dx.doi.org/10.1145/358769.358784)

1. Jim N. Gray, Raymond A. Lorie, Gianfranco R. Putzolu, and Irving L. Traiger:
    “[Granularity of Locks and Degrees of Consistency in a Shared Data Base](http://citeseer.ist.psu.edu/viewdoc/download?doi=10.1.1.92.8248&rep=rep1&type=pdf),” in *Modelling in Data
    Base Management Systems: Proceedings of the IFIP Working Conference on Modelling in Data Base
    Management Systems*, edited by G. M. Nijssen, pages
    364–394, Elsevier/North Holland Publishing, 1976. Also in *Readings in Database Systems*, 4th edition, edited by Joseph M.
    Hellerstein and Michael Stonebraker, MIT Press, 2005. ISBN: 978-0-262-69314-1

1. Kapali P. Eswaran, Jim N. Gray, Raymond A. Lorie, and Irving L. Traiger:
    “[The Notions of Consistency and Predicate Locks in a Database System](http://research.microsoft.com/en-us/um/people/gray/papers/On%20the%20Notions%20of%20Consistency%20and%20Predicate%20Locks%20in%20a%20Database%20System%20CACM.pdf),” *Communications of the
    ACM*, volume 19, number 11, pages 624–633, November 1976.

    > 深入理解事务
    >
    > ……它们大多数都沿用了和 IBM 于 1975 年推出的第一个 SQL 数据库 System R[1-3] 相似的总体设计

1. “[ACID Transactions Are Incredibly Helpful](http://web.archive.org/web/20150320053809/https://foundationdb.com/acid-claims),” FoundationDB, LLC, 2013.

1. John D. Cook:
    “[ACID Versus BASE for Database Transactions](http://www.johndcook.com/blog/2009/07/06/brewer-cap-theorem-base/),” *johndcook.com*, July 6, 2009.

1. Gavin Clarke:
    “[NoSQL's CAP Theorem Busters: We Don't Drop ACID](http://www.theregister.co.uk/2012/11/22/foundationdb_fear_of_cap_theorem/),” *theregister.co.uk*, November 22, 2012.

    > 深入理解事务
    >
    > ……随着这种新型分布式数据库的炒作，很多人开始认为事务与可扩展性时相对立的两面，而大规模系统为了性能和高可用性将不得不牺牲事务的支持[5，6]

1. Theo Härder and Andreas Reuter:
    “[Principles of Transaction-Oriented Database Recovery](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.87.2812&rep=rep1&type=pdf),” *ACM Computing Surveys*,
    volume 15, number 4, pages 287–317, December 1983.
    [doi:10.1145/289.291](http://dx.doi.org/10.1145/289.291)

1. Peter Bailis, Alan Fekete, Ali Ghodsi, et al.:
    “[HAT, not CAP: Towards Highly Available Transactions](http://www.bailis.org/papers/hat-hotos2013.pdf),”
    at *14th USENIX Workshop on Hot Topics in Operating Systems* (HotOS), May 2013.

    > ACID 的含义
    >
    > ……例如，我们稍后就会看到，围绕着”隔离性“就存在很多含糊不清的争议

1. Armando Fox, Steven D. Gribble, Yatin Chawathe, et al.:
    “[Cluster-Based Scalable Network Services](http://www.cs.berkeley.edu/~brewer/cs262b/TACC.pdf),” at
    *16th ACM Symposium on Operating Systems Principles* (SOSP), October 1997.

    > ACID 的含义
    >
    > ……不符合 ACID 标准的系统有时被冠以 BASE，取另外几个特性的首字母，基本可用性（Basically Available），软状态（Soft state）和最终一致性（Eventual consistency）

1. Philip A. Bernstein, Vassos Hadzilacos, and Nathan Goodman:
    [*Concurrency Control and Recovery in Database Systems*](http://research.microsoft.com/en-us/people/philbe/ccontrol.aspx).
    Addison-Wesley, 1987. ISBN: 978-0-201-10715-9, available online at *research.microsoft.com*.

    > 隔离性
    >
    > ……虽然实际上它们可能同时运行，但数据库系统要确保当事务提交时，其结果与串行执行完全相同

1. Alan Fekete, Dimitrios Liarokapis, Elizabeth O'Neil, et al.:
      “[Making Snapshot Isolation Serializable](https://www.cse.iitb.ac.in/infolab/Data/Courses/CS632/2009/Papers/p492-fekete.pdf),” *ACM Transactions on Database Systems*,
      volume 30, number 2, pages 492–528, June 2005.
      [doi:10.1145/1071610.1071615](http://dx.doi.org/10.1145/1071610.1071615)

      > 隔离性
      >
      > ……

1. Mai Zheng, Joseph Tucek, Feng Qin, and Mark Lillibridge:
      “[Understanding   the Robustness of SSDs Under Power Fault](https://www.usenix.org/system/files/conference/fast13/fast13-final80.pdf),” at *11th USENIX Conference on File and
      Storage Technologies* (FAST), February 2013.

      > 

1. Laurie Denness:
      “[SSDs: A Gift and a Curse](https://laur.ie/blog/2015/06/ssds-a-gift-and-a-curse/),”
      *laur.ie*, June 2, 2015.

1. Adam Surak:
      “[When Solid State   Drives Are Not That Solid](https://blog.algolia.com/when-solid-state-drives-are-not-that-solid/),” *blog.algolia.com*, June 15, 2015.

      > 复制与持久性
      >
      > ……当电源突然断电时，特别对于固态硬盘可能发生意外：连 fsync 之后的数据也不能保证可以正确恢复[12]。和所有其他类型的软件类似，磁盘的固件也可能存在 bug[13，14]

1. Thanumalayan Sankaranarayana Pillai, Vijay Chidambaram,
      Ramnatthan Alagappan, et al.: “[All   File Systems Are Not Created Equal: On the Complexity of Crafting Crash-Consistent Applications](http://research.cs.wisc.edu/wind/Publications/alice-osdi14.pdf),”
      at *11th USENIX Symposium on Operating Systems Design and Implementation* (OSDI),
      October 2014.

1. Chris Siebenmann:
      “[Unix's File Durability   Problem](https://utcc.utoronto.ca/~cks/space/blog/unix/FileSyncProblem),” *utcc.utoronto.ca*, April 14, 2016.

      > 复制与持久性
      >
      > ……考虑到数据库存储引擎与文件系统之间复杂而微妙的关系，其中也可能包含难以追踪的 bug，并最终导致在系统发生崩溃后，磁盘上的文件也出现损坏[15，16]

1. Lakshmi N. Bairavasundaram, Garth R.
      Goodson, Bianca Schroeder, et al.:
      “[An Analysis of Data   Corruption in the Storage Stack](http://research.cs.wisc.edu/adsl/Publications/corruption-fast08.pdf),” at *6th USENIX Conference on File and Storage
      Technologies* (FAST), February 2008.

      > 复制与持久性
      >
      > ……磁盘上的数据可能悄无声息地出现损坏但又没有被及时检测到

1. Bianca Schroeder, Raghav Lagisetty, and Arif Merchant:
      “[Flash   Reliability in Production: The Expected and the Unexpected](https://www.usenix.org/conference/fast16/technical-sessions/presentation/schroeder),” at *14th USENIX Conference on
      File and Storage Technologies* (FAST), February 2016.

      > 复制与持久性
      >
      > ……一项关于固态硬盘的研究发现，在部署的前四年，30% 到 80% 的固态盘至少发生一个坏块

1. Don Allison:
      “[SSD Storage – Ignorance of Technology Is No   Excuse](https://blog.korelogic.com/blog/2015/03/24),” *blog.korelogic.com*, March 24, 2015.

      > 复制与持久性
      >
      > ……某些固态盘如果遭遇突然断电，可能会在接下来的几周内发生丢失数据情况，温度在里面起了关键性作用

1. Dave Scherer:
      “[Those Are Not Transactions (Cassandra 2.0)](http://web.archive.org/web/20150526065247/http://blog.foundationdb.com/those-are-not-transactions-cassandra-2-0),” *blog.foundationdb.com*, September 6, 2013.

1. Kyle Kingsbury:
      “[Call Me Maybe: Cassandra](http://aphyr.com/posts/294-call-me-maybe-cassandra/),”
      *aphyr.com*, September 24, 2013.

1. “[ACID Support in Aerospike](https://web.archive.org/web/20170305002118/https://www.aerospike.com/docs/architecture/assets/AerospikeACIDSupport.pdf),” Aerospike, Inc., June 2014.

      > 单对象写入
      >
      > ……虽然 compare-and-set 和其他单对象操作有时也被称为“轻量级事务”，甚至”ACID"[20-22]，但这里其实存在一些误导性

1. Martin Kleppmann:
      “[Hermitage: Testing the 'I' in ACID](http://martin.kleppmann.com/2014/11/25/hermitage-testing-the-i-in-acid.html),” *martin.kleppmann.com*, November 25, 2014.

      > 弱隔离级别
      >
      > ……这些弱隔离级别理解起来更为困难，甚至可能带来一些难以琢磨的隐患，但在实践中还是被广泛使用

1. Tristan D'Agosta:
      “[BTC Stolen from Poloniex](https://bitcointalk.org/index.php?topic=499580),”
      *bitcointalk.org*, March 4, 2014.

1. bitcointhief2:
      “[How I Stole Roughly 100 BTC from an Exchange and How I Could Have Stolen More!](http://www.reddit.com/r/Bitcoin/comments/1wtbiu/how_i_stole_roughly_100_btc_from_an_exchange_and/),” *reddit.com*,
      February 2, 2014.

1. Sudhir Jorwekar, Alan Fekete, Krithi Ramamritham, and S. Sudarshan:
      “[Automating the Detection of Snapshot Isolation Anomalies](http://www.vldb.org/conf/2007/papers/industrial/p1263-jorwekar.pdf),” at *33rd International Conference on
      Very Large Data Bases* (VLDB), September 2007.

1. Michael Melanson:
      “[Transactions: The Limits of Isolation](https://www.michaelmelanson.net/transactions-the-limits-of-isolation/),”
      *michaelmelanson.net*, November 30, 2014.

      > 弱隔离级别
      >
      > ……弱隔离所引发的并发性错误绝非仅是理论存在，它们已经造成了大量的资金损失[24，25]，审计部门的调查[26]，以及客户数据损坏[27]等

1. Hal Berenson, Philip A. Bernstein, Jim N. Gray, et al.:
      “[A Critique of ANSI SQL Isolation Levels](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/tr-95-51.pdf),”
      at *ACM International Conference on Management of Data* (SIGMOD), May 1995.

1. Atul Adya: “[Weak Consistency: A Generalized Theory and Optimistic Implementations for Distributed Transactions](http://pmg.csail.mit.edu/papers/adya-phd.pdf),”
      PhD Thesis, Massachusetts Institute of Technology, March 1999.

1. Peter Bailis, Aaron Davidson, Alan Fekete, et al.:
      “[Highly Available Transactions: Virtues and Limitations (Extended Version)](http://arxiv.org/pdf/1302.0309.pdf),” at *40th International Conference on Very Large Data Bases*
      (VLDB), September 2014.

      > 弱隔离级别
      >
      > ……如果你需要的是严格、正式的定义和分析，可以参考文献[28-30]

1. Bruce Momjian:
      “[MVCC Unmasked](http://momjian.us/main/presentations/internals.html#mvcc),” *momjian.us*,
      July 2014.

1. Annamalai Gurusami:
      “[Repeatable Read Isolation Level in InnoDB – How Consistent Read View Works](https://web.archive.org/web/20161225080947/https://blogs.oracle.com/mysqlinnodb/entry/repeatable_read_isolation_level_in),”
      *blogs.oracle.com*, January 15, 2013.

      > 快照级别隔离和可重复读
      >
      > ……快照级别隔离非常流行，目前大多数关系型数据库都已经支持[31、32]

1. Nikita Prokopov:
      “[Unofficial Guide to Datomic Internals](http://tonsky.me/blog/unofficial-guide-to-datomic-internals/),” *tonsky.me*, May 6, 2014.

1. Baron Schwartz:
      “[Immutability, MVCC, and Garbage Collection](http://www.xaprb.com/blog/2013/12/28/immutability-mvcc-and-garbage-collection/),” *xaprb.com*, December 28, 2013.

1. J. Chris Anderson, Jan Lehnardt, and Noah Slater:
      *CouchDB: The Definitive Guide*. O'Reilly Media, 2010.
      ISBN: 978-0-596-15589-6

      > 索引与快照级别隔离
      >
      > ……CouchDB、Datomic 和 LMDB 则使用另一种方法。它们主体结构是 B-tree，但采用了一种追加/写时复制的技术，当需要更新时，不会修改现有的页面，而总是创建一个新的修改副本，拷贝必要的内容，然后让父节点，或者递归向上直到树的 root 结点都指向新创建的结点。那些不受更新影响的页面都不需要复制，保持不变并被父节点所指向[33-35]

1. Rikdeb Mukherjee:
      “[Isolation in DB2 (Repeatable Read, Read Stability, Cursor Stability, Uncommitted Read) with Examples](http://mframes.blogspot.co.uk/2013/07/isolation-in-cursor.html),”
      *mframes.blogspot.co.uk*, July 4, 2013.

1. Steve Hilker:
      “[Cursor Stability (CS) – IBM DB2 Community](https://web.archive.org/web/20150420001721/http://www.toadworld.com/platforms/ibmdb2/w/wiki/6661.cursor-stability-cs.aspx),”
      *toadworld.com*, March 14, 2013.

      > 原子写操作
      >
      > ……原子操作通常采用对读取对象加独占锁的方式来实现，这样在更新被提交之前不会有其他事务可以读它。这种技术有时被称为游标稳定性[36，37]

1. Nate Wiger:
      “[An Atomic Rant](https://nateware.com/2010/02/18/an-atomic-rant/),” *nateware.com*,
      February 18, 2010.

      > 原子写操作
      >
      > ……不过，基于对象关系映射（ORM）框架可以很容易地就产生出来非“读-修改-写回”的应用层代码，导致无法使用数据库所提供的原子操作

1. Joel Jacobson:
      “[Riak 2.0: Data Types](https://web.archive.org/web/20161023195905/http://blog.joeljacobson.com/riak-2-0-data-types/),”
      *blog.joeljacobson.com*, March 23, 2014.

      > 冲突解决与复制
      >
      > ……Riak 2.0 新数据类型的设计思路，当一个值被不同的客户端同时更新时，Riak 自动将更新合并在一起，避免发生更新丢失

1. Michael J. Cahill, Uwe Röhm, and Alan Fekete:
      “[Serializable Isolation for Snapshot Databases](http://www.cs.nyu.edu/courses/fall12/CSCI-GA.2434-001/p729-cahill.pdf),” at *ACM International Conference on
      Management of Data* (SIGMOD), June 2008.
      [doi:10.1145/1376616.1376690](http://dx.doi.org/10.1145/1376616.1376690)

1. Dan R. K. Ports and Kevin Grittner:
      “[Serializable Snapshot Isolation in PostgreSQL](http://drkp.net/papers/ssi-vldb12.pdf),”
      at *38th International Conference on Very Large Databases* (VLDB), August 2012.

      > 写倾斜与幻读
      >
      > ……通常，医院会安排多个医生值班，医生也可以申请调整班次，但前提是确保至少一位医生还在该班次中值班

1. Tony Andrews:
      “[Enforcing   Complex Constraints in Oracle](http://tonyandrews.blogspot.co.uk/2004/10/enforcing-complex-constraints-in.html),” *tonyandrews.blogspot.co.uk*, October 15, 2004.

      > 定义写倾斜
      >
      > ……至少一名医生值班这样的要求涉及对多个对象进行约束，目前大多数数据库不支持这种类型约束，所以取决于具体的数据库，开发者可能采用触发器或物化视图来自己实现类似约束

1. Douglas B. Terry, Marvin M. Theimer, Karin Petersen, et al.:
      “[Managing   Update Conflicts in Bayou, a Weakly Connected Replicated Storage System](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.141.7889&rep=rep1&type=pdf),” at
      *15th ACM Symposium on Operating Systems Principles* (SOSP), December 1995.
      [doi:10.1145/224056.224070](http://dx.doi.org/10.1145/224056.224070)

      > 会议室预订系统
      >
      > ……假设要求同一时间、同一个会议室不能被预订两次

1. Gary Fredericks:
      “[Postgres Serializability   Bug](https://github.com/gfredericks/pg-serializability-bug),” *github.com*, September 2015.

1. Michael Stonebraker, Samuel Madden, Daniel J. Abadi, et al.:
      “[The End of an Architectural Era (It’s Time for a Complete Rewrite)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.137.3697&rep=rep1&type=pdf),” at *33rd International
      Conference on Very Large Data Bases* (VLDB), September 2007.

      > 实际串行支持
      >
      > ……解决并发问题最直接的方法是避免并发……但数据库设计人员直到 2007 年前后才完全确信，采用单线程循环来执行事务是可行的

1. John Hugg:
      “[H-Store/VoltDB Architecture vs. CEP Systems and Newer Streaming Architectures](https://www.youtube.com/watch?v=hD5M4a1UVz8),”
      at *Data @Scale Boston*, November 2014.

1. Robert Kallman, Hideaki Kimura, Jonathan Natkins, et al.:
      “[H-Store: A High-Performance, Distributed Main Memory Transaction Processing System](http://www.vldb.org/pvldb/vol1/1454211.pdf),”
      *Proceedings of the VLDB Endowment*, volume 1, number 2, pages 1496–1499, August 2008.

1. Rich Hickey:
      “[The Architecture of Datomic](http://www.infoq.com/articles/Architecture-Datomic),” *infoq.com*, November 2, 2012.

      > 实际串行执行
      >
      > ……VoltDB/H-Store、Redis 和 Dotamic 等采用串行方式执行事务

1. John Hugg:
      “[Debunking Myths About the VoltDB In-Memory Database](https://dzone.com/articles/debunking-myths-about-voltdb),” *dzone.com*, May 28, 2014.

      > 分区
      >
      > ……VoltDB 报告的跨区事务吞吐量大约只有 1000 次/秒，这比单分区吞吐量低了好几个数量级，而且没法通过增加更多机器的方式来扩展性能

1. Joseph M. Hellerstein, Michael Stonebraker, and James Hamilton:
      “[Architecture of a Database System](https://dsf.berkeley.edu/papers/fntdb07-architecture.pdf),”
      *Foundations and Trends in Databases*, volume 1, number 2, pages 141–259, November 2007.
      [doi:10.1561/1900000002](http://dx.doi.org/10.1561/1900000002)

      > 索引区间锁
      >
      > ……因此，大多数使用 2PL 的数据库实际上实现的是索引区间锁，本质上它是对谓词锁的简化或者近似

1. Michael J. Cahill:
      “[Serializable Isolation for Snapshot Databases](http://cahill.net.au/wp-content/uploads/2010/02/cahill-thesis.pdf),” PhD Thesis, University of Sydney, July 2009.

      > 可串行化的快照隔离
      >
      > ……SSI 算法面试至今不过数年，它于 2008 年被首次提出[40]，后来成为 Michael Cahill 的博士论文研究主题

1. D. Z. Badal:
      “[Correctness of Concurrency Control and Implications in Distributed Databases](http://ieeexplore.ieee.org/abstract/document/762563/),” at *3rd International IEEE Computer Software and
      Applications Conference* (COMPSAC), November 1979.

1. Rakesh Agrawal, Michael J. Carey, and Miron Livny:
      “[Concurrency Control Performance Modeling: Alternatives and Implications](http://www.eecs.berkeley.edu/~brewer/cs262/ConcControl.pdf),” *ACM Transactions on Database
      Systems* (TODS), volume 12, number 4, pages 609–654, December 1987.
      [doi:10.1145/32204.32220](http://dx.doi.org/10.1145/32204.32220)

      > 悲观与乐观的并发控制
      >
      > ……乐观并发控制其实是一个古老的想法[52]，关于其优点和缺点已经争论了很长时间[53]

1. Dave Rosenthal:
      “[Databases at 14.4MHz](http://web.archive.org/web/20150427041746/http://blog.foundationdb.com/databases-at-14.4mhz),”
      *blog.foundationdb.com*, December 10, 2014.

      > 可串行化快照隔离的性能
      >
      > ……FoundationDB 将冲突检查分布在多台机器上，从而提高总体吞吐量。即使数据可能跨多台机器进行分区，事务也可以在多个分区上读、写数据并保证可串行化隔离

