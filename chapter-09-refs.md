Designing Data-Intensive Applications
=====================================

Chapter 9 Consistency and Consensus
--------------------

1. Peter Bailis and Ali Ghodsi:
    “[Eventual Consistency Today: Limitations, Extensions, and Beyond](http://queue.acm.org/detail.cfm?id=2462076),” *ACM Queue*, volume 11, number 3, pages 55-63, March 2013.
    [doi:10.1145/2460276.2462076](http://dx.doi.org/10.1145/2460276.2462076)

    > 一致性保证
    >
    > ……而在收敛之前，读请求可能返回任何值甚至读失败

1. Prince Mahajan, Lorenzo Alvisi, and Mike Dahlin:
    “[Consistency, Availability, and Convergence](http://apps.cs.utexas.edu/tech_reports/reports/tr/TR-2036.pdf),” University of Texas at Austin, Department of Computer
    Science, Tech Report UTCS TR-11-22, May 2011.

    > 一致性保证
    >
    > ……换言之，最终一致性意味着“收敛”，即预期所有的副本最终会收敛到相同的值

1. Alex Scotti:
    “[Adventures in Building Your Own Database](http://www.slideshare.net/AlexScotti1/allyourbase-55212398),” at *All Your Base*, November 2015.

    > 一致性保证
    >
    > ……数据库表面上看起来像一个可以进行读写的变量，但事实上他内部有无比复杂的更多语义要求

1. Peter Bailis, Aaron Davidson, Alan Fekete, et al.:
    “[Highly Available Transactions: Virtues and Limitations](http://arxiv.org/pdf/1302.0309.pdf),” at *40th International Conference on Very Large Data Bases* (VLDB),
    September 2014. Extended version published as pre-print arXiv:1302.0309 &#91;cs.DB&#93;.

1. Paolo Viotti and Marko Vukolić:
    “[Consistency in Non-Transactional Distributed Storage Systems](http://arxiv.org/abs/1512.00168),” arXiv:1512.00168, 12 April 2016.

    > 一致性保证
    >
    > ……分布式一致性模型与我们之前讨论过的多种事务隔离级别有相似之处[4，5]

1. Maurice P. Herlihy and Jeannette M. Wing:
    “[Linearizability: A Correctness Condition for Concurrent Objects](http://cs.brown.edu/~mph/HerlihyW90/p463-herlihy.pdf),” *ACM Transactions on Programming
    Languages and Systems* (TOPLAS), volume 12, number 3, pages 463–492, July 1990.
    [doi:10.1145/78969.78972](http://dx.doi.org/10.1145/78969.78972)

1. Leslie Lamport:
    “[On interprocess communication](https://www.microsoft.com/en-us/research/publication/interprocess-communication-part-basic-formalism-part-ii-algorithms/),”
    *Distributed Computing*, volume 1, number 2, pages 77–101, June 1986.
    [doi:10.1007/BF01786228](http://dx.doi.org/10.1007/BF01786228)

1. David K. Gifford:
    “[Information Storage in a Decentralized Computer System](http://www.mirrorservice.org/sites/www.bitsavers.org/pdf/xerox/parc/techReports/CSL-81-8_Information_Storage_in_a_Decentralized_Computer_System.pdf),” Xerox Palo Alto Research Centers, CSL-81-8, June 1981.

    > 可线性化
    >
    > ……这就是可线性化[6]（也称为原子一致性[7]，强一致性等[8]）的思想

1. Martin Kleppmann:
    “[Please Stop Calling Databases CP or AP](http://martin.kleppmann.com/2015/05/11/please-stop-calling-databases-cp-or-ap.html),” *martin.kleppmann.com*, May 11, 2015.

    > 图9-1显示了一个非线性化体育网站的例子[9]。爱丽丝和鲍勃坐在同一个房间里，都在查看他们的手机，看2014年世界杯决赛的结果。就在最终比分公布后，爱丽丝刷新了页面，看到冠军公布，并兴奋地告诉鲍勃。鲍勃难以置信地在自己的手机上点击重新加载，但他的请求进入了一个滞后的数据库副本，因此他的手机显示比赛仍在进行。

1. Kyle Kingsbury:
    “[Call Me Maybe: MongoDB Stale Reads](https://aphyr.com/posts/322-call-me-maybe-mongodb-stale-reads),” *aphyr.com*, April 20, 2015.

    > 我们可以进一步细化这个时序图，将每个操作在某个时间点上原子化地生效可视化。一个更复杂的例子见图9-4[10]。

1. Kyle Kingsbury:
      “[Computational Techniques in Knossos](https://aphyr.com/posts/314-computational-techniques-in-knossos),” *aphyr.com*, May 17, 2014.

      > 这是线性化背后的直觉；正式定义[6]更精确地描述了它。通过记录所有请求和响应的时间，并检查它们是否可以被安排成有效的顺序，来测试一个系统的行为是否可线性化是可能的（尽管计算上很昂贵）[11]。

1. Peter Bailis:
      “[Linearizability   Versus Serializability](http://www.bailis.org/blog/linearizability-versus-serializability/),” *bailis.org*, September 24, 2014.

      > 可序列化是事务的一个隔离属性，每个事务可以读写多个对象（行、文档、记录）--参见 "单对象和多对象操作"。它保证事务的行为与它们按某种序列顺序执行的情况相同（每个事务在下一个事务开始之前运行完毕）。该序列顺序与事务实际运行的顺序不同是可以的[12]。

1. Philip A. Bernstein, Vassos Hadzilacos, and Nathan Goodman:
      [*Concurrency Control and Recovery in Database Systems*](http://research.microsoft.com/en-us/people/philbe/ccontrol.aspx).
      Addison-Wesley, 1987. ISBN: 978-0-201-10715-9, available online at *research.microsoft.com*.

      > 一个数据库可以同时提供可序列化和可线性化，这种组合被称为严格的可序列化或强单拷贝可序列化（strong-1SR）[4, 13]。基于两阶段锁定（见 "两阶段锁定（2PL）"）或实际串行执行（见 "实际串行执行"）的可序列化实现通常是可线性的。

1. Mike Burrows:
      “[The Chubby Lock Service for Loosely-Coupled Distributed Systems](https://research.google/pubs/pub27897/),”
      at *7th USENIX Symposium on Operating System Design and Implementation* (OSDI), November 2006.

      > 一个使用单领导复制的系统需要确保确实只有一个领导，而不是几个（分脑）。选举领导者的一种方法是使用一个锁：每个启动的节点都试图获得这个锁，成功的节点就成为领导者[14]。无论这种锁是如何实现的，它必须是可线性的：所有节点必须同意哪个节点拥有这个锁；否则它就没有用。

1. Flavio P. Junqueira and Benjamin Reed:
      *ZooKeeper: Distributed Process Coordination*. O'Reilly Media, 2013.
      ISBN: 978-1-449-36130-3

1. “[etcd Documentation](https://etcd.io/docs/),” The Linux Foundation, *etcd.io*.

1. “[Apache Curator](http://curator.apache.org/),” Apache Software Foundation, *curator.apache.org*, 2015.

      > 像Apache ZooKeeper[15]和etcd[16]这样的协调服务经常被用来实现分布式锁和领导者选举。它们使用共识算法，以容错的方式实现可线性化的操作（我们在本章后面的 "容错共识 "中讨论了这种算法）。iii 要正确实现锁和领导者选举，还有许多微妙的细节（例如，见 "领导者和锁 "中的围栏问题），像Apache Curator[17]这样的库通过在ZooKeeper之上提供更高级别的配方来帮助。然而，一个可线性化的存储服务是这些协调任务的基本基础。

1. Morali Vallath:
      *Oracle 10g RAC Grid, Services & Clustering*. Elsevier Digital Press, 2006.
      ISBN: 978-1-555-58321-7

      > 在一些分布式数据库中，分布式锁定也被用在更细的层面上，比如Oracle Real Application Clusters（RAC）[18]。RAC对每个磁盘页使用一个锁，多个节点共享对同一磁盘存储系统的访问。由于这些可线性化的锁在交易执行的关键路径上，RAC的部署通常有一个专门的集群互连网络用于数据库节点之间的通信。

1. Peter Bailis, Alan Fekete, Michael J Franklin, et al.:
      “[Coordination-Avoiding Database Systems](http://arxiv.org/pdf/1402.2237.pdf),”
      *Proceedings of the VLDB Endowment*, volume 8, number 3, pages 185–196, November 2014.

      > 然而，一个硬的唯一性约束，比如你通常在关系数据库中发现的那种，需要线性化。其他类型的约束，如外键或属性约束，可以在不需要线性化的情况下实现

1. Kyle Kingsbury:
      “[Call Me Maybe: etcd and Consul](https://aphyr.com/posts/316-call-me-maybe-etcd-and-consul),” *aphyr.com*, June 9, 2014.

      > 使用领导者进行读取依赖于一个假设，即你肯定知道谁是领导者。正如在 "真理是由多数人定义的 "中所讨论的，一个节点很有可能认为它是领导者，而事实上它不是--如果这个妄想的领导者继续提供请求，它很可能违反线性化[20]。在异步复制的情况下，故障转移甚至可能失去已承诺的写入（见 "处理节点中断"），这违反了耐久性和线性化。

1. Flavio P. Junqueira, Benjamin C. Reed, and Marco Serafini:
      “[Zab: High-Performance Broadcast for Primary-Backup Systems](https://marcoserafini.github.io/papers/zab.pdf),”
      at *41st IEEE International Conference on Dependable Systems and Networks* (DSN), June 2011.
      [doi:10.1109/DSN.2011.5958223](http://dx.doi.org/10.1109/DSN.2011.5958223)

1. Diego Ongaro and John K. Ousterhout:
      “[In Search of an Understandable Consensus Algorithm](https://www.usenix.org/system/files/conference/atc14/atc14-paper-ongaro.pdf),”
      at *USENIX Annual Technical Conference* (ATC), June 2014.

      > 一些共识算法，我们将在本章后面讨论，与单领导复制有相似之处。然而，共识协议包含了防止分脑和陈旧复制的措施。由于这些细节，共识算法可以安全地实现可线性化存储。例如，ZooKeeper[21]和etcd[22]就是这样工作的。 

1. Hagit Attiya, Amotz Bar-Noy, and Danny Dolev:
      “[Sharing Memory Robustly in Message-Passing Systems](http://www.cse.huji.ac.il/course/2004/dist/p124-attiya.pdf),”
      *Journal of the ACM*, volume 42, number 1, pages 124–142, January 1995.
      [doi:10.1145/200836.200869](http://dx.doi.org/10.1145/200836.200869)

1. Nancy Lynch and Alex Shvartsman:
      “[Robust Emulation of Shared Memory Using Dynamic Quorum-Acknowledged Broadcasts](http://groups.csail.mit.edu/tds/papers/Lynch/FTCS97.pdf),” at *27th Annual International Symposium on
      Fault-Tolerant Computing* (FTCS), June 1997.
      [doi:10.1109/FTCS.1997.614100](http://dx.doi.org/10.1109/FTCS.1997.614100)

1. Christian Cachin, Rachid Guerraoui, and Luís Rodrigues:
      [*Introduction to Reliable and Secure Distributed Programming*](http://www.distributedprogramming.net/),
      2nd edition. Springer, 2011. ISBN: 978-3-642-15259-7,
      [doi:10.1007/978-3-642-15260-3](http://dx.doi.org/10.1007/978-3-642-15260-3)

1. Sam Elliott, Mark Allen, and Martin Kleppmann:
      [personal communication](https://twitter.com/lenary/status/654761711933648896),
      thread on *twitter.com*, October 15, 2015.

1. Niklas Ekström, Mikhail Panchenko, and Jonathan Ellis:
      “[Possible Issue with Read Repair?](http://mail-archives.apache.org/mod_mbox/cassandra-dev/201210.mbox/%3CFA480D1DC3964E2C8B0A14E0880094C9%40Robotech%3E),” email thread on *cassandra-dev* mailing list, October 2012.

      > 有趣的是，有可能使Dynamo式的四元组线性化，但代价是性能下降：读者必须同步执行读修复（见 "读修复和反熵"），然后再将结果返回给应用程序[23]，而写者必须在发送其写内容之前读取一个四元组节点的最新状态[24, 25]。然而，Riak并不执行同步的读修复，因为这对性能有影响[26]。Cassandra确实在法定人数的读取中等待读取修复的完成[27]，但由于它使用了最后写入的冲突解决方法，如果有多个并发的写到同一个键上，它就失去了线性化。

1. Maurice P. Herlihy:
      “[Wait-Free Synchronization](https://cs.brown.edu/~mph/Herlihy91/p124-herlihy.pdf),”
      *ACM Transactions on Programming Languages and Systems* (TOPLAS), volume 13, number 1,
      pages 124–149, January 1991.
      [doi:10.1145/114005.102808](http://dx.doi.org/10.1145/114005.102808)

1. Armando Fox and Eric A. Brewer:
      “[Harvest, Yield, and Scalable Tolerant Systems](http://radlab.cs.berkeley.edu/people/fox/static/pubs/pdf/c18.pdf),” at *7th Workshop on Hot Topics in Operating
      Systems* (HotOS), March 1999.
      [doi:10.1109/HOTOS.1999.798396](http://dx.doi.org/10.1109/HOTOS.1999.798396)

1. Seth Gilbert and Nancy Lynch:
      “[Brewer’s Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web Services](http://www.comp.nus.edu.sg/~gilbert/pubs/BrewersConjecture-SigAct.pdf),”
      *ACM SIGACT News*, volume 33, number 2, pages 51–59, June 2002.
      [doi:10.1145/564585.564601](http://dx.doi.org/10.1145/564585.564601)

1. Seth Gilbert and Nancy Lynch:
      “[Perspectives on the CAP Theorem](http://groups.csail.mit.edu/tds/papers/Gilbert/Brewer2.pdf),” *IEEE Computer Magazine*, volume 45, number 2, pages 30–36, February 2012.
      [doi:10.1109/MC.2011.389](http://dx.doi.org/10.1109/MC.2011.389)

1. Eric A. Brewer:
      “[CAP Twelve Years Later: How the 'Rules' Have Changed](http://cs609.cs.ua.edu/CAP12.pdf),” *IEEE Computer Magazine*, volume 45, number 2, pages 23–29, February 2012.
      [doi:10.1109/MC.2012.37](http://dx.doi.org/10.1109/MC.2012.37)

1. Susan B. Davidson, Hector Garcia-Molina, and Dale Skeen:
      “[Consistency in Partitioned Networks](http://delab.csd.auth.gr/~dimitris/courses/mpc_fall05/papers/invalidation/acm_csur85_partitioned_network_consistency.pdf),” *ACM Computing Surveys*, volume 17, number 3, pages 341–370, September 1985.
      [doi:10.1145/5505.5508](http://dx.doi.org/10.1145/5505.5508)

1. Paul R. Johnson and Robert H. Thomas:
      “[RFC 677: The Maintenance of Duplicate Databases](https://tools.ietf.org/html/rfc677),” Network Working Group, January 27, 1975.

1. Bruce G. Lindsay, Patricia Griffiths Selinger, C. Galtieri, et al.:
      “[Notes on Distributed Databases](http://domino.research.ibm.com/library/cyberdig.nsf/papers/A776EC17FC2FCE73852579F100578964/$File/RJ2571.pdf),” IBM Research, Research Report RJ2571(33471), July 1979.

1. Michael J. Fischer and Alan Michael:
      “[Sacrificing Serializability to Attain High Availability of Data in an Unreliable Network](http://www.cs.ucsb.edu/~agrawal/spring2011/ugrad/p70-fischer.pdf),” at
      *1st ACM Symposium on Principles of Database Systems* (PODS), March 1982.
      [doi:10.1145/588111.588124](http://dx.doi.org/10.1145/588111.588124)

      > 因此，不需要线性化的应用对网络问题的容忍度更高。这一见解被普遍称为CAP定理[29, 30, 31, 32]，由Eric Brewer在2000年命名，尽管自20世纪70年代以来，分布式数据库的设计者就已经知道这一权衡[33, 34, 35, 36]。

1. Eric A. Brewer:
      “[NoSQL: Past, Present, Future](http://www.infoq.com/presentations/NoSQL-History),”
      at *QCon San Francisco*, November 2012.

      > CAP最初是作为一个经验法则提出的，没有精确的定义，目的是开始讨论数据库的权衡问题。当时，许多分布式数据库专注于在共享存储的机器集群上提供可线性化的语义[18]，而CAP鼓励数据库工程师探索分布式无共享系统的更广泛的设计空间，这更适合于实现大规模的网络服务[37]。CAP对这种文化转变功不可没--看看2000年代中期以来新数据库技术的爆炸性增长（被称为NoSQL）。

1. Henry Robinson:
      “[CAP Confusion: Problems with 'Partition Tolerance,'](https://web.archive.org/web/20160304020135/http://blog.cloudera.com/blog/2010/04/cap-confusion-problems-with-partition-tolerance/)”
      *blog.cloudera.com*, April 26, 2010.

      > CAP有时被表述为一致性、可用性、分区容忍度：从3个中选2个。不幸的是，这样说有误导性[32]，因为网络分区是一种故障，所以它们不是你可以选择的东西：无论你喜欢与否，它们都会发生[38]。

1. Adrian Cockcroft:
      “[Migrating to Microservices](http://www.infoq.com/presentations/migration-cloud-native),” at *QCon London*, March 2014.

      > 在网络正常工作的时候，一个系统可以同时提供一致性（线性化）和总可用性。当网络发生故障时，你必须在可线性化或完全可用性之间做出选择。因此，CAP的一个更好的表述方式是：要么是一致性，要么是分区时的可用性[39]。一个更可靠的网络需要较少地做出这种选择，但在某些时候，这种选择是不可避免的。

1. Martin Kleppmann:
      “[A Critique of the CAP Theorem](http://arxiv.org/abs/1509.05393),” arXiv:1509.05393,
      September 17, 2015.

      > 在关于CAP的讨论中，对可用性一词有几个相互矛盾的定义，作为定理的形式化[30]也与它的通常含义不相符[40]。许多所谓的 "高可用"（容错）系统实际上并不符合CAP对可用性的特异性定义。总而言之，围绕CAP有很多误解和混乱，它不能帮助我们更好地理解系统，所以最好避免使用CAP。

1. Nancy A. Lynch:
      “[A Hundred Impossibility Proofs for Distributed Computing](http://groups.csail.mit.edu/tds/papers/Lynch/podc89.pdf),” at *8th ACM Symposium on Principles of Distributed
      Computing* (PODC), August 1989.
      [doi:10.1145/72981.72982](http://dx.doi.org/10.1145/72981.72982)

1. Hagit Attiya, Faith Ellen, and Adam Morrison:
      “[Limitations of Highly-Available Eventually-Consistent Data Stores](https://www.cs.tau.ac.il/~mad/publications/podc2015-replds.pdf),”
      at *ACM Symposium on Principles of Distributed Computing* (PODC), July 2015.
      [doi:10.1145/2767386.2767419](http://dx.doi.org/10.1145/2767386.2767419)

      > 在分布式系统中有许多更有趣的不可能结果[41]，而且CAP现在已经被更精确的结果所取代[2，42]，所以它在今天主要是具有历史意义。

1. Peter Sewell, Susmit Sarkar,
      Scott Owens, et al.:
      “[x86-TSO: A Rigorous and Usable Programmer's Model for x86 Multiprocessors](http://www.cl.cam.ac.uk/~pes20/weakmemory/cacm.pdf),” *Communications of the ACM*,
      volume 53, number 7, pages 89–97, July 2010.
      [doi:10.1145/1785414.1785443](http://dx.doi.org/10.1145/1785414.1785443)

1. Martin Thompson:
      “[Memory Barriers/Fences](http://mechanical-sympathy.blogspot.co.uk/2011/07/memory-barriersfences.html),” *mechanical-sympathy.blogspot.co.uk*, July 24, 2011.

      > 尽管可线性化是一个有用的保证，但实际上很少有系统是可线性化的。例如，即使是现代多核CPU上的RAM也是不可线性化的[43]：如果在一个CPU核上运行的线程写到一个内存地址，而另一个CPU核上的线程在不久之后读取相同的地址，它不能保证读取第一个线程写的值（除非使用内存屏障或栅栏[44]）。

1. Ulrich Drepper:
      “[What Every Programmer Should Know About Memory](http://www.akkadia.org/drepper/cpumemory.pdf),” *akkadia.org*, November 21, 2007.

      > 这种行为的原因是，每个CPU核都有自己的内存缓存和存储缓冲区。默认情况下，内存访问首先进入缓存，任何变化都会异步写入主内存。由于访问缓存中的数据要比访问主内存快得多[45]，这一特性对于现代CPU的良好性能是至关重要的。然而，现在有几份数据（一份在主内存中，可能还有几份在不同的缓存中），这些副本是异步更新的，所以线性化就消失了。

1. Daniel J. Abadi:
      “[Consistency Tradeoffs in Modern Distributed Database System Design](http://cs-www.cs.yale.edu/homes/dna/papers/abadi-pacelc.pdf),” *IEEE Computer Magazine*,
      volume 45, number 2, pages 37–42, February 2012.
      [doi:10.1109/MC.2012.33](http://dx.doi.org/10.1109/MC.2012.33)

      > 许多选择不提供可线性化保证的分布式数据库也是如此：它们这样做主要是为了提高性能，而不是为了容错[46]。可线性化的速度很慢--这在任何时候都是如此，不仅仅是在网络故障期间。

1. Hagit Attiya and Jennifer L. Welch:
      “[Sequential Consistency Versus Linearizability](http://courses.csail.mit.edu/6.852/01/papers/p91-attiya.pdf),” *ACM Transactions on Computer Systems* (TOCS),
      volume 12, number 2, pages 91–122, May 1994.
      [doi:10.1145/176575.176576](http://dx.doi.org/10.1145/176575.176576)

      > 难道我们不能找到一种更有效的可线性化存储的实现方式吗？似乎答案是否定的。Attiya和Welch[47]证明，如果你想要线性化，读写请求的响应时间至少与网络中延迟的不确定性成正比。

1. Mustaque Ahamad, Gil Neiger, James E. Burns, et al.:
      “[Causal   Memory: Definitions, Implementation, and Programming](http://www-i2.informatik.rwth-aachen.de/i2/fileadmin/user_upload/documents/Seminar_MCMM11/Causal_memory_1996.pdf),” *Distributed
      Computing*, volume 9, number 1, pages 37–49, March 1995.
      [doi:10.1007/BF01784241](http://dx.doi.org/10.1007/BF01784241)

1. Wyatt Lloyd, Michael J. Freedman,
      Michael Kaminsky, and David G. Andersen:
      “[Stronger Semantics for Low-Latency Geo-Replicated Storage](https://www.usenix.org/system/files/conference/nsdi13/nsdi13-final149.pdf),” at *10th USENIX Symposium on Networked
      Systems Design and Implementation* (NSDI), April 2013.

1. Marek Zawirski, Annette Bieniusa, Valter Balegas, et al.:
      “[SwiftCloud: Fault-Tolerant Geo-Replication Integrated All the Way to the Client Machine](http://arxiv.org/abs/1310.3107),” INRIA Research Report 8347, August 2013.

1. Peter Bailis, Ali Ghodsi, Joseph M Hellerstein, and Ion Stoica:
      “[Bolt-on Causal Consistency](http://db.cs.berkeley.edu/papers/sigmod13-bolton.pdf),” at
      *ACM International Conference on Management of Data* (SIGMOD), June 2013.

      > 在许多情况下，看起来需要线性化的系统实际上只需要因果一致性，这可以更有效地实现。基于这一观察，研究人员正在探索新类型的数据库，这些数据库保留了因果关系，其性能和可用性特征与最终一致的系统相似[49, 50, 51]。

1. Philippe Ajoux, Nathan Bronson, Sanjeev
      Kumar, et al.:
      “[Challenges to Adopting Stronger Consistency at Scale](https://www.usenix.org/system/files/conference/hotos15/hotos15-paper-ajoux.pdf),” at *15th USENIX Workshop on Hot Topics in
      Operating Systems* (HotOS), May 2015.

1. Peter Bailis:
      “[Causality Is Expensive (and What to Do About It)](http://www.bailis.org/blog/causality-is-expensive-and-what-to-do-about-it/),” *bailis.org*, February 5, 2014.

      > 由于这项研究是相当新的，还没有多少进入生产系统，而且还有一些挑战需要克服[52, 53]。然而，它是未来系统的一个有希望的方向。

1. Ricardo Gonçalves, Paulo Sérgio Almeida,
      Carlos Baquero, and Victor Fonte:
      “[Concise Server-Wide Causality Management for Eventually Consistent Data Stores](http://haslab.uminho.pt/tome/files/global_logical_clocks.pdf),” at *15th IFIP International
      Conference on Distributed Applications and Interoperable Systems* (DAIS), June 2015.
      [doi:10.1007/978-3-319-19129-4_6](http://dx.doi.org/10.1007/978-3-319-19129-4_6)

      > 确定哪个操作发生在哪个操作之前的技术，与我们在 "检测并发写入 "中讨论的类似。那一节讨论了无领导数据存储中的因果关系，我们需要检测对同一键的并发写操作，以防止丢失更新。因果一致性更进一步：它需要跟踪整个数据库的因果关系，而不仅仅是单个键的因果关系。版本向量可以被概括为做这个[54]。

1. Rob Conery:
      “[A Better ID   Generator for PostgreSQL](http://rob.conery.io/2014/05/29/a-better-id-generator-for-postgresql/),” *rob.conery.io*, May 29, 2014.

1. Leslie Lamport:
      “[Time, Clocks, and the Ordering of Events in a Distributed System](https://www.microsoft.com/en-us/research/publication/time-clocks-ordering-events-distributed-system/),”
      *Communications of the ACM*, volume 21, number 7, pages 558–565, July 1978.
      [doi:10.1145/359545.359563](http://dx.doi.org/10.1145/359545.359563)

      > 为了确保没有其他节点正在以相同的用户名和较低的时间戳同时创建一个账户，你将不得不检查其他每个节点，看看它正在做什么[56]。如果其他节点之一发生故障或由于网络问题而无法联系到，这个系统就会陷入停顿。这不是我们需要的那种容错系统。

1. Xavier Défago, André Schiper, and Péter Urbán:
      “[Total Order Broadcast and Multicast Algorithms: Taxonomy and Survey](https://dspace.jaist.ac.jp/dspace/bitstream/10119/4883/1/defago_et_al.pdf),” *ACM Computing
      Surveys*, volume 36, number 4, pages 372–421, December 2004.
      [doi:10.1145/1041680.1041682](http://dx.doi.org/10.1145/1041680.1041682)

1. Hagit Attiya and Jennifer Welch: *Distributed
      Computing: Fundamentals, Simulations and Advanced Topics*, 2nd edition.
      John Wiley & Sons, 2004. ISBN: 978-0-471-45324-6,
      [doi:10.1002/0471478210](http://dx.doi.org/10.1002/0471478210)

      > 如前所述，单领导复制通过选择一个节点作为领导，并在领导的单个CPU核心上对所有操作进行排序来确定总的操作顺序。那么，挑战在于，如果吞吐量大于单个领导者所能处理的，如何扩展系统，以及如何处理领导者失败时的故障转移（见 "处理节点故障"）。在分布式系统文献中，这个问题被称为总序广播或原子广播[25, 57, 58]。

1. Mahesh
      Balakrishnan, Dahlia Malkhi, Vijayan Prabhakaran, et al.:
      “[CORFU: A Shared Log Design for Flash Clusters](https://www.usenix.org/system/files/conference/nsdi12/nsdi12-final30.pdf),” at *9th USENIX Symposium on Networked
      Systems Design and Implementation* (NSDI), April 2012.

      > 每个分区有一个领导者的分区数据库通常只维护每个分区的排序，这意味着它们不能提供跨分区的一致性保证（例如，一致的快照、外键引用）。在所有分区之间进行总排序是可能的，但需要额外的协调[59]。

1. Fred B. Schneider:
      “[Implementing Fault-Tolerant Services Using the State Machine Approach: A Tutorial](http://www.cs.cornell.edu/fbs/publications/smsurvey.pdf),” *ACM Computing Surveys*, volume
      22, number 4, pages 299–319, December 1990.

      > 总的顺序广播正是数据库复制所需要的：如果每条消息都代表对数据库的写，而每个副本都以相同的顺序处理相同的写，那么这些副本就会彼此保持一致（除了任何暂时的复制滞后）。这个原则被称为状态机复制[60]，我们将在第11章中回到这个问题。

1. Alexander Thomson, Thaddeus Diamond, Shu-Chun Weng, et al.:
      “[Calvin: Fast Distributed Transactions for Partitioned Database Systems](http://cs.yale.edu/homes/thomson/publications/calvin-sigmod12.pdf),” at *ACM International Conference
      on Management of Data* (SIGMOD), May 2012.

      > 类似地，总序广播可以用来实现可序列化的事务：正如在 "实际序列执行 "中所讨论的，如果每条消息都代表一个要作为存储过程执行的确定性事务，并且如果每个节点都以相同的顺序处理这些消息，那么数据库的分区和副本就会保持相互一致[61]。

1. Mahesh Balakrishnan, Dahlia Malkhi, Ted Wobber, et al.:
      “[Tango: Distributed Data Structures over a Shared Log](https://www.microsoft.com/en-us/research/publication/tango-distributed-data-structures-over-a-shared-log/),”
      at *24th ACM Symposium on Operating Systems Principles* (SOSP), November 2013.
      [doi:10.1145/2517349.2522732](http://dx.doi.org/10.1145/2517349.2522732)

1. Robbert van Renesse and Fred B. Schneider:
      “[Chain Replication for Supporting High Throughput and Availability](http://static.usenix.org/legacy/events/osdi04/tech/full_papers/renesse/renesse.pdf),” at *6th USENIX
      Symposium on Operating System Design and Implementation* (OSDI), December 2004.

      > 你可以通过使用总序广播作为一个只附加的日志来实现这样一个可线性化的比较和设置的操作，如下所示[62, 63]。

1. Leslie Lamport:
      “[How to Make a Multiprocessor Computer That Correctly Executes Multiprocess Programs](https://lamport.azurewebsites.net/pubs/multi.pdf),”
      *IEEE Transactions on Computers*, volume 28, number 9, pages 690–691, September 1979.
      [doi:10.1109/TC.1979.1675439](http://dx.doi.org/10.1109/TC.1979.1675439)

1. Enis Söztutar, Devaraj Das, and Carter Shanklin:
      “[Apache HBase High Availability at the Next Level](https://web.archive.org/web/20160405122821/http://hortonworks.com/blog/apache-hbase-high-availability-next-level/),”
      *hortonworks.com*, January 22, 2015.

1. Brian F Cooper, Raghu Ramakrishnan, Utkarsh Srivastava, et al.:
      “[PNUTS: Yahoo!’s Hosted Data Serving Platform](http://www.mpi-sws.org/~druschel/courses/ds/papers/cooper-pnuts.pdf),” at *34th International Conference on Very Large Data
      Bases* (VLDB), August 2008.
      [doi:10.14778/1454159.1454167](http://dx.doi.org/10.14778/1454159.1454167)

      > 虽然这个过程确保了可线性化的写入，但它并不保证可线性化的读取--如果你从一个从日志中异步更新的存储中读取，它可能是过时的。(准确地说，这里描述的程序提供了顺序一致性[47, 64]，有时也被称为时间线一致性[65, 66]，是比线性化稍弱的保证）。为了使读数可线性化，有几个选择。

1. Tushar Deepak Chandra and Sam Toueg:
      “[Unreliable Failure Detectors for Reliable Distributed Systems](http://courses.csail.mit.edu/6.852/08/papers/CT96-JACM.pdf),” *Journal of the ACM*,
      volume 43, number 2, pages 225–267, March 1996.
      [doi:10.1145/226643.226647](http://dx.doi.org/10.1145/226643.226647)

      > 这并不是巧合：可以证明，可线性化的比较-设置（或增量-获取）寄存器和总序广播都等同于共识[28, 67]。也就是说，如果你能解决这些问题中的一个，你就能把它转化为其他问题的解决方案。这是一个相当深刻和令人惊讶的洞察力!

1. Michael J. Fischer, Nancy Lynch, and Michael S. Paterson:
      “[Impossibility of Distributed Consensus with One Faulty Process](https://groups.csail.mit.edu/tds/papers/Lynch/jacm85.pdf),” *Journal of the ACM*, volume 32, number 2, pages 374–382, April 1985.
      [doi:10.1145/3149.214121](http://dx.doi.org/10.1145/3149.214121)

      > 你可能听说过FLP结果[68]--以作者Fischer、Lynch和Paterson的名字命名--该结果证明，如果存在节点崩溃的风险，没有任何算法能够始终达成共识。在一个分布式系统中，我们必须假设节点可能崩溃，所以可靠的共识是不可能的。然而，我们在这里讨论的是达成共识的算法。这到底是怎么回事？

1. Michael Ben-Or: “Another Advantage of Free
      Choice: Completely Asynchronous Agreement Protocols,” at *2nd ACM Symposium on Principles of
      Distributed Computing* (PODC), August 1983.
      [doi:10.1145/800221.806707](http://dl.acm.org/citation.cfm?id=806707)

      > 答案是，FLP结果是在异步系统模型中证明的（见 "系统模型和现实"），这是一个非常有限制性的模型，它假设了一个不能使用任何时钟或超时的确定性算法。如果允许算法使用超时，或以其他方式识别疑似崩溃的节点（即使这种怀疑有时是错误的），那么共识就变得可解[67]。即使只是允许算法使用随机数，也足以绕过不可能的结果[69]。

1. Jim N. Gray and Leslie Lamport:
      “[Consensus on Transaction Commit](http://db.cs.berkeley.edu/cs286/papers/paxoscommit-tods2006.pdf),” *ACM Transactions on Database Systems* (TODS), volume 31,
      number 1, pages 133–160, March 2006.
      [doi:10.1145/1132863.1132867](http://dx.doi.org/10.1145/1132863.1132867)

1. Rachid Guerraoui:
      “[Revisiting the Relationship Between Non-Blocking Atomic Commitment and Consensus](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.27.6456&rep=rep1&type=pdf),”
      at *9th International Workshop on Distributed Algorithms* (WDAG), September 1995.
      [doi:10.1007/BFb0022140](http://dx.doi.org/10.1007/BFb0022140)

      > 在这一节中，我们将首先更详细地研究原子提交问题。特别是，我们将讨论两阶段提交（2PC）算法，这是最常见的解决原子提交的方法，在各种数据库、消息传递系统和应用服务器中都有实现。事实证明，2PC是一种共识算法--但不是一种很好的算法[70, 71]。

1. Thanumalayan Sankaranarayana Pillai, Vijay Chidambaram,
      Ramnatthan Alagappan, et al.: “[All File Systems Are Not Created Equal: On the Complexity of Crafting Crash-Consistent Applications](http://research.cs.wisc.edu/wind/Publications/alice-osdi14.pdf),”
      at *11th USENIX Symposium on Operating Systems Design and Implementation* (OSDI),
      October 2014.

      > 因此，在单个节点上，交易承诺关键取决于数据被持久地写入磁盘的顺序：首先是数据，然后是提交记录[72]。决定交易是提交还是中止的关键时刻是磁盘完成写入提交记录的时刻：在这个时刻之前，仍有可能中止（由于崩溃），但在这个时刻之后，交易就被提交了（即使数据库崩溃了）。因此，是一个单一的设备（一个特定的磁盘驱动器的控制器，连接到一个特定的节点）使提交成为原子性的。

1. Jim Gray:
      “[The Transaction Concept: Virtues and Limitations](http://jimgray.azurewebsites.net/papers/thetransactionconcept.pdf),”
      at *7th International Conference on Very Large Data Bases* (VLDB), September 1981.

1. Hector Garcia-Molina and Kenneth Salem:
      “[Sagas](http://www.cs.cornell.edu/andru/cs711/2002fa/reading/sagas.pdf),” at
      *ACM International Conference on Management of Data* (SIGMOD), May 1987.
      [doi:10.1145/38713.38742](http://dx.doi.org/10.1145/38713.38742)

      > (一个已提交的事务的影响有可能在以后被另一个补偿性的事务所撤销[73, 74]。然而，从数据库的角度来看，这是一个单独的事务，因此任何跨事务的正确性要求都是应用程序的问题）。

1. C. Mohan, Bruce G. Lindsay, and Ron Obermarck:
      “[Transaction Management in the R* Distributed Database Management System](https://cs.brown.edu/courses/csci2270/archives/2012/papers/dtxn/p378-mohan.pdf),”
      *ACM Transactions on Database Systems*, volume 11, number 4, pages 378–396, December 1986.
      [doi:10.1145/7239.7266](http://dx.doi.org/10.1145/7239.7266)

1. “[Distributed Transaction Processing: The XA Specification](http://pubs.opengroup.org/onlinepubs/009680699/toc.pdf),” X/Open Company Ltd., Technical Standard
      XO/CAE/91/300, December 1991. ISBN: 978-1-872-63024-3

1. Mike Spille:
      “[XA Exposed, Part II](http://www.jroller.com/pyrasun/entry/xa_exposed_part_ii_schwartz),”
      *jroller.com*, April 3, 2004.

1. Ivan Silva Neto and Francisco Reverbel:
      “[Lessons Learned from Implementing WS-Coordination and WS-AtomicTransaction](http://www.ime.usp.br/~reverbel/papers/icis2008.pdf),” at *7th IEEE/ACIS International Conference on
      Computer and Information Science* (ICIS), May 2008.
      [doi:10.1109/ICIS.2008.75](http://dx.doi.org/10.1109/ICIS.2008.75)

1. James E. Johnson, David E. Langworthy, Leslie Lamport, and Friedrich H. Vogt:
      “[Formal Specification of a Web Services Protocol](https://www.microsoft.com/en-us/research/publication/formal-specification-of-a-web-services-protocol/),”
      at *1st International Workshop on Web Services and Formal Methods* (WS-FM), February 2004.
      [doi:10.1016/j.entcs.2004.02.022](http://dx.doi.org/10.1016/j.entcs.2004.02.022)

      > 两阶段提交是一种在多个节点上实现原子事务提交的算法--即确保所有节点提交或所有节点中止。它是分布式数据库中的一种经典算法[13, 35, 75]。2PC在一些数据库内部使用，也以XA事务的形式提供给应用程序[76, 77]（例如，由Java Transaction API支持）或通过SOAP网络服务的WS-AtomicTransaction[78, 79]。

1. Dale Skeen:
      “[Nonblocking Commit Protocols](http://www.cs.utexas.edu/~lorenzo/corsi/cs380d/papers/Ske81.pdf),” at *ACM International Conference on Management of Data* (SIGMOD), April 1981.
      [doi:10.1145/582318.582339](http://dx.doi.org/10.1145/582318.582339)

      > 作为2PC的替代方案，有人提出了一种叫做三阶段提交（3PC）的算法[13, 80]。然而，3PC假设网络的延迟是有界的，节点的响应时间是有界的；在大多数实际系统中，网络延迟和进程停顿是无界的（见第八章），它不能保证原子性。

1. Gregor Hohpe:
      “[Your Coffee Shop Doesn’t Use Two-Phase Commit](http://www.martinfowler.com/ieeeSoftware/coffeeShop.pdf),” *IEEE Software*, volume 22, number 2, pages 64–66, March 2005.
      [doi:10.1109/MS.2005.52](http://dx.doi.org/10.1109/MS.2005.52)

1. Pat Helland:
      “[Life Beyond Distributed Transactions: An Apostate’s Opinion](http://www-db.cs.wisc.edu/cidr/cidr2007/papers/cidr07p15.pdf),” at *3rd Biennial Conference on Innovative Data Systems
      Research* (CIDR), January 2007.

1. Jonathan Oliver:
      “[My Beef with MSDTC and Two-Phase Commits](http://blog.jonathanoliver.com/my-beef-with-msdtc-and-two-phase-commits/),” *blog.jonathanoliver.com*, April 4, 2011.

1. Oren Eini (Ahende Rahien):
      “[The Fallacy of Distributed Transactions](http://ayende.com/blog/167362/the-fallacy-of-distributed-transactions),” *ayende.com*, July 17, 2014.

1. Clemens Vasters:
      “[Transactions in Windows Azure (with Service Bus) – An Email Discussion](https://blogs.msdn.microsoft.com/clemensv/2012/07/30/transactions-in-windows-azure-with-service-bus-an-email-discussion/),” *vasters.com*, July 30, 2012.

1. “[Understanding Transactionality in Azure](https://docs.particular.net/nservicebus/azure/understanding-transactionality-in-azure),” NServiceBus Documentation, Particular Software, 2015.

      > 分布式事务，特别是那些用两阶段提交实现的事务，有一个混合的声誉。一方面，它们被视为提供了重要的安全保障，否则很难实现；另一方面，它们被批评为造成了操作问题，扼杀了性能，并承诺超过它们所能提供的[81, 82, 83, 84]。许多云服务选择不实施分布式交易，因为它们会产生操作问题[85, 86]。

1. Randy Wigginton, Ryan Lowe, Marcos Albe, and Fernando Ipar:
      “[Distributed Transactions in MySQL](https://web.archive.org/web/20161010054152/https://www.percona.com/live/mysql-conference-2013/sites/default/files/slides/XA_final.pdf),”
      at *MySQL Conference and Expo*, April 2013.

1. Mike Spille:
      “[XA Exposed, Part I](https://web.archive.org/web/20130523064202/http://www.jroller.com/pyrasun/entry/xa_exposed),”
      *jroller.com*, April 3, 2004.

      > 一些分布式事务的实现会带来严重的性能损失--例如，据报道，MySQL中的分布式事务比单节点事务慢10倍以上[87]，所以当人们建议不要使用它们时，也就不奇怪了。两阶段提交所固有的性能成本大部分是由于崩溃恢复所需的额外磁盘强制（fsync）[88]，以及额外的网络往返次数。

1. Ajmer Dhariwal:
      “[Orphaned MSDTC Transactions (-2 spids)](http://www.eraofdata.com/orphaned-msdtc-transactions-2-spids/),” *eraofdata.com*, December 12, 2008.

1. Paul Randal:
      “[Real World Story of DBCC PAGE Saving the Day](http://www.sqlskills.com/blogs/paul/real-world-story-of-dbcc-page-saving-the-day/),” *sqlskills.com*, June 19, 2013.

      > 理论上，如果协调器崩溃并被重新启动，它应该从日志中干净地恢复其状态并解决任何疑问中的事务。然而，在实践中，无主的疑问中事务确实发生了[89, 90]--也就是说，协调器由于某种原因不能决定结果的事务（例如，由于软件错误导致的事务日志丢失或损坏）。这些交易不能被自动解决，所以它们在数据库中永远存在，持有锁并阻止其他交易。

1. “[in-doubt xact resolution Server Configuration Option](https://msdn.microsoft.com/en-us/library/ms179586.aspx),” SQL Server 2016 documentation, Microsoft, Inc.,
      2016.

      > 许多XA的实现都有一个紧急避风港，叫做启发式决策：允许参与者单方面决定中止或提交一个有疑问的事务，而不需要协调者的明确决定[76, 77, 91]。明确地说，这里的启发式是一种委婉的说法，即可能破坏了原子性，因为它违反了两阶段提交中的承诺体系。因此，启发式决策只是为了摆脱灾难性的情况，而不是为了正常使用。

1. Cynthia Dwork, Nancy Lynch, and Larry Stockmeyer:
      “[Consensus in the Presence of Partial Synchrony](http://www.net.t-labs.tu-berlin.de/~petr/ADC-07/papers/DLS88.pdf),” *Journal of the ACM*, volume 35, number 2, pages 288–323,
      April 1988. [doi:10.1145/42282.42283](http://dx.doi.org/10.1145/42282.42283)

      > 因此，终止属性受制于少于一半的节点崩溃或不可达的假设。然而，大多数共识的实现都能确保安全属性--协议、完整性和有效性--始终得到满足，即使大多数节点失效或出现严重的网络问题[92]。因此，大规模的故障可以使系统无法处理请求，但它不能破坏共识系统，使其做出无效的决定。

1. Miguel Castro and Barbara H. Liskov:
      “[Practical Byzantine Fault Tolerance and Proactive Recovery](http://zoo.cs.yale.edu/classes/cs426/2012/bib/castro02practical.pdf),” *ACM Transactions on Computer Systems*,
      volume 20, number 4, pages 396–461, November 2002.
      [doi:10.1145/571637.571640](http://dx.doi.org/10.1145/571637.571640)

      > 大多数共识算法假定不存在拜占庭故障，如 "拜占庭故障 "中所讨论的。也就是说，如果一个节点没有正确遵守协议（例如，如果它向不同的节点发送矛盾的信息），它可能会破坏协议的安全属性。只要少于三分之一的节点有拜占庭故障，就有可能使共识对拜占庭故障具有鲁棒性[25, 93]，但我们没有空间在本书中详细讨论这些算法。

1. Brian M. Oki and Barbara H. Liskov:
      “[Viewstamped Replication: A New Primary Copy Method to Support Highly-Available Distributed Systems](http://www.cs.princeton.edu/courses/archive/fall11/cos518/papers/viewstamped.pdf),” at
      *7th ACM Symposium on Principles of Distributed Computing* (PODC), August 1988.
      [doi:10.1145/62546.62549](http://dx.doi.org/10.1145/62546.62549)

1. Barbara H. Liskov and James Cowling:
      “[Viewstamped Replication Revisited](http://pmg.csail.mit.edu/papers/vr-revisited.pdf),”
      Massachusetts Institute of Technology, Tech Report MIT-CSAIL-TR-2012-021, July 2012.

1. Leslie Lamport:
      “[The Part-Time Parliament](https://www.microsoft.com/en-us/research/publication/part-time-parliament/),”
      *ACM Transactions on Computer Systems*, volume 16, number 2, pages 133–169, May 1998.
      [doi:10.1145/279227.279229](http://dx.doi.org/10.1145/279227.279229)

1. Leslie Lamport:
      “[Paxos Made Simple](https://www.microsoft.com/en-us/research/publication/paxos-made-simple/),” *ACM SIGACT News*, volume 32, number 4, pages 51–58, December 2001.

1. Tushar Deepak Chandra, Robert Griesemer, and Joshua
      Redstone: “[Paxos Made Live – An Engineering Perspective](http://www.read.seas.harvard.edu/~kohler/class/08w-dsi/chandra07paxos.pdf),” at *26th ACM Symposium on Principles of Distributed
      Computing* (PODC), June 2007.

1. Robbert
      van Renesse: “[Paxos Made Moderately Complex](http://www.cs.cornell.edu/home/rvr/Paxos/paxos.pdf),” *cs.cornell.edu*, March 2011.

1. Diego Ongaro:
      “[Consensus: Bridging Theory and Practice](https://github.com/ongardie/dissertation),”
      PhD Thesis, Stanford University, August 2014.

1. Heidi Howard, Malte Schwarzkopf, Anil Madhavapeddy,
      and Jon Crowcroft: “[Raft Refloated: Do We Have Consensus?](http://www.cl.cam.ac.uk/~ms705/pub/papers/2015-osr-raft.pdf),” *ACM SIGOPS Operating Systems Review*, volume 49,
      number 1, pages 12–21, January 2015.
      [doi:10.1145/2723872.2723876](http://dx.doi.org/10.1145/2723872.2723876)

1. André Medeiros:
      “[ZooKeeper’s Atomic Broadcast Protocol: Theory and Practice](http://www.tcs.hut.fi/Studies/T-79.5001/reports/2012-deSouzaMedeiros.pdf),” Aalto University School of Science, March 20, 2012.

1. Robbert van Renesse, Nicolas Schiper, and
      Fred B. Schneider: “[Vive La Différence: Paxos vs. Viewstamped Replication vs. Zab](http://arxiv.org/abs/1309.5671),” *IEEE Transactions on Dependable and Secure Computing*,
      volume 12, number 4, pages 472–484, September 2014.
      [doi:10.1109/TDSC.2014.2355848](http://dx.doi.org/10.1109/TDSC.2014.2355848)

1. Will
      Portnoy: “[Lessons Learned from Implementing Paxos](http://blog.willportnoy.com/2012/06/lessons-learned-from-paxos.html),” *blog.willportnoy.com*, June 14, 2012.

      > 最著名的容错共识算法是Viewstamped Replication (VSR) [94, 95], Paxos [96, 97, 98, 99], Raft [22, 100, 101], 和Zab [15, 21, 102]。这些算法之间有相当多的相似之处，但它们并不一样[103]。在本书中，我们不会对不同算法的全部细节进行讨论：只要知道它们有一些共同的高层次想法就足够了，除非你自己要实现一个共识系统（这可能是不可取的--这很难[98, 104]）。

1. Heidi Howard, Dahlia Malkhi, and Alexander Spiegelman:
      “[Flexible Paxos: Quorum Intersection Revisited](https://drops.dagstuhl.de/opus/volltexte/2017/7094/pdf/LIPIcs-OPODIS-2016-25.pdf),”
      at *20th International Conference on Principles of Distributed Systems* (OPODIS), December 2016.
      [doi:10.4230/LIPIcs.OPODIS.2016.25](http://dx.doi.org/10.4230/LIPIcs.OPODIS.2016.25)

      > 相反，它必须从节点的法定人数中收集投票（见 "读写的法定人数"）。对于领导者想要做出的每一个决定，它必须将提议的值发送给其他节点，并等待法定人数的节点对提议作出支持的回应。法定人数通常由大多数节点组成，但并不总是这样[105]。一个节点只有在不知道有任何其他领导者有更高的历时的情况下才会投票赞成一项提议。

1. Heidi Howard and Jon Crowcroft:
      “[Coracle: Evaluating Consensus at the Internet Edge](http://www.sigcomm.org/sites/default/files/ccr/papers/2015/August/2829988-2790010.pdf),”
      at *Annual Conference of the ACM Special Interest Group on Data Communication* (SIGCOMM), August 2015.
      [doi:10.1145/2829988.2790010](http://dx.doi.org/10.1145/2829988.2790010)

1. Kyle Kingsbury:
      “[Call Me Maybe: Elasticsearch 1.5.0](https://aphyr.com/posts/323-call-me-maybe-elasticsearch-1-5-0),” *aphyr.com*, April 27, 2015.

      > 这些任务可以通过明智地使用ZooKeeper中的原子操作、短暂节点和通知来实现。如果操作得当，这种方法可以让应用程序自动从故障中恢复，而无需人工干预。这并不容易，尽管像Apache Curator[17]这样的库已经出现，在ZooKeeper客户端API的基础上提供更高级别的工具--但它仍然比试图从头开始实现必要的共识算法要好得多，后者的成功记录很差[107]。

1. Ivan Kelly:
      “[BookKeeper Tutorial](https://github.com/ivankelly/bookkeeper-tutorial),”
      *github.com*, October 2014.

      > 通常情况下，ZooKeeper管理的那种数据是相当缓慢变化的：它代表了诸如 "运行在10.1.1.23上的节点是第7分区的领导者 "这样的信息，它可能在几分钟或几小时的时间尺度内发生变化。它不是用来存储应用程序的运行状态的，它可能每秒变化数千甚至数百万次。如果应用程序的状态需要从一个节点复制到另一个节点，可以使用其他工具（如Apache BookKeeper [108]）。

1. Camille Fournier:
      “[Consensus Systems for the Skeptical Architect](https://vimeo.com/102667163),”
      at *Philly ETE*, Philadelphia, PA, USA, April 2014.

      > 然而，服务发现是否真的需要达成共识还不太清楚。DNS是查询服务名称的IP地址的传统方式，它使用多层缓存来实现良好的性能和可用性。从DNS中的读取绝对不是线性的，如果DNS查询的结果有点陈旧，通常不被认为有问题[109]。更重要的是，DNS是可靠可用的，并且对网络中断具有鲁棒性。

1. Kenneth P. Birman:
      “[A History of the Virtual Synchrony Replication Model](https://ptolemy.berkeley.edu/projects/truststc/pubs/713/History%20of%20the%20Virtual%20Synchrony%20Replication%20Model%202010.pdf),”
      in *Replication: Theory and Practice*, Springer LNCS volume 5959, chapter 6, pages 91–120, 2010.
      ISBN: 978-3-642-11293-5, [doi:10.1007/978-3-642-11294-2_6](http://dx.doi.org/10.1007/978-3-642-11294-2_6)

      > ZooKeeper和朋友们可以被看作是会员服务研究的悠久历史的一部分，这种研究可以追溯到20世纪80年代，对建立高度可靠的系统非常重要，例如空中交通管制[110]。

