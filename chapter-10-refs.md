Designing Data-Intensive Applications
=====================================

Chapter 10 Batch Processing
--------------------

1. Jeffrey Dean and Sanjay Ghemawat:
    “[MapReduce: Simplified Data Processing on Large Clusters](https://research.google/pubs/pub62/),”
    at *6th USENIX Symposium on Operating System Design and Implementation* (OSDI), December 2004.

1. Joel Spolsky:
    “[The Perils of JavaSchools](https://www.joelonsoftware.com/2005/12/29/the-perils-of-javaschools-2/),” *joelonsoftware.com*, December 29, 2005.

    > 著名批处理算法 MapReduce[1] 使得 Google 具有如此大规模的可扩展性能力（虽然该说法有些夸大和简单化）[2]

1. Shivnath Babu and Herodotos Herodotou:
    “[Massively Parallel Databases and MapReduce Systems](https://www.microsoft.com/en-us/research/wp-content/uploads/2013/11/db-mr-survey-final.pdf),”
    *Foundations and Trends in Databases*, volume 5, number 1, pages 1–104, November 2013.
    [doi:10.1561/1900000036](http://dx.doi.org/10.1561/1900000036)

1. David J. DeWitt and Michael Stonebraker:
    “[MapReduce: A Major Step Backwards](https://homes.cs.washington.edu/~billhowe/mapreduce_a_major_step_backwards.html),” originally published at *databasecolumn.vertica.com*, January 17, 2008.

    > 与多年前为数据仓库开发的并行处理系统相比，MapReduce 是一个相当低级别的编程模型

1. Henry Robinson:
    “[The Elephant Was a Trojan Horse: On the Death of Map-Reduce at Google](https://www.the-paper-trail.org/post/2014-06-25-the-elephant-was-a-trojan-horse-on-the-death-of-map-reduce-at-google/),”
    *the-paper-trail.org*, June 25, 2014.

    > 虽然MapReduce 的重要性现在有些下降，但它仍然值得深入理解，因为它清晰地解释了批处理为什么有用以及如何有用

1. “[The Hollerith Machine](https://www.census.gov/history/www/innovations/technology/the_hollerith_tabulator.html),” United States Census Bureau, *census.gov*.

    > 打孔制表机（例如1890年美国人口普查[6]中使用的 Hlooerith 机器）就实现了半机械化的批量处理

1. “[IBM 82, 83, and 84 Sorters Reference Manual](http://www.textfiles.com/bitsavers/pdf/ibm/punchedCard/Sorter/A24-1034-1_82-83-84_sorters.pdf),” Edition A24-1034-1, International Business
    Machines Corporation, July 1962.

    > MapReduce 与 1940 年和1950 年广泛应用与商业数据处理的 IBM 卡片分类机器有着惊人的相似之处

1. Adam Drake:
    “[Command-Line Tools Can Be 235x Faster than Your Hadoop Cluster](http://aadrake.com/command-line-tools-can-be-235x-faster-than-your-hadoop-cluster.html),” *aadrake.com*, January 25, 2014.

    > 简单日志处理
    >
    > ……使用 awk，sed，grep，sort，uniq 和 xargs 的组合，可以在几分钟内完成许多数据分析任务，并且表现令人十分满意

1. “[GNU Coreutils 8.23 Documentation](http://www.gnu.org/software/coreutils/manual/html_node/index.html),” Free Software Foundation, Inc., 2014.

    > 排序与内存中聚合
    >
    > ……GNU Coreutils（Linux）中的 sort 实用程序通过自动唤出到磁盘的方式支持处理大于内存的数据集，且排序可以自动并行化以充分利用多核 CPU

1. Martin Kleppmann:
    “[Kafka, Samza, and the Unix Philosophy of Distributed Data](http://martin.kleppmann.com/2015/08/05/kafka-samza-unix-philosophy-distributed-data.html),” *martin.kleppmann.com*, August 5, 2015.

    > UNIX 哲学
    >
    > ……我们更深入地研究一下，目的是从这挖掘、借鉴一些不错的想法

1. Doug McIlroy:
      [Internal Bell Labs memo](https://swtch.com/~rsc/thread/mdmpipe.pdf),
      October 1964. Cited in: Dennis M. Richie:
      “[Advice from Doug McIlroy](https://www.bell-labs.com/usr/dmr/www/mdmpipe.html),”
      *bell-labs.com*.

      > UNIX 哲学
      >
      > ……UNIX 管道的发明者 Doug Mcilroy 在 1964 年首先描述了这种用例

1. M. D. McIlroy, E. N. Pinson, and B. A. Tague:
      “[UNIX Time-Sharing System: Foreword](https://archive.org/details/bstj57-6-1899),”
      *The Bell System Technical Journal*, volume 57, number 6, pages 1899–1904,
      July 1978.

1. Eric S. Raymond:
      [*The Art of UNIX Programming*](http://www.catb.org/~esr/writings/taoup/html/).
      Addison-Wesley, 2003. ISBN: 978-0-13-142901-7

      > UNIX 哲学
      >
      > ……对于这种哲学有了更为完整的描述[12，13]
      >
      > ……这种方法（自动化、快速原型设计、增量式迭代、测试友好、分解为可管理的模块等）听起来像今天的敏捷开发与 DevOps 运动

1. Ronald Duncan:
      “[Text File Formats – ASCII Delimited Text – Not CSV or TAB Delimited Text](https://ronaldduncan.wordpress.com/2009/10/31/text-file-formats-ascii-delimited-text-not-csv-or-tab-delimited-text/),”
      *ronaldduncan.wordpress.com*, October 31, 2009.

      > 统一接口
      >
      > ……

1. Alan Kay:
      “[Is 'Software Engineering' an Oxymoron?](http://tinlizzie.org/~takashi/IsSoftwareEngineeringAnOxymoron.pdf),” *tinlizzie.org*.

1. Martin Fowler:
      “[InversionOfControl](http://martinfowler.com/bliki/InversionOfControl.html),”
      *martinfowler.com*, June 26, 2005.

1. Daniel J. Bernstein:
      “[Two File Descriptors for Sockets](http://cr.yp.to/tcpip/twofd.html),” *cr.yp.to*.

1. Rob Pike and Dennis M. Ritchie:
      “[The Styx Architecture for Distributed Systems](http://doc.cat-v.org/inferno/4th_edition/styx),” *Bell Labs Technical Journal*, volume 4, number 2, pages
      146–152, April 1999.

      > 然而，你能用stdin和stdout做的事情是有限的。需要多个输入或输出的程序是可能的，但很棘手。如果一个程序直接打开文件进行读写，或启动另一个程序作为子进程，或打开网络连接，那么这个I/O是由程序本身来连接的[17, 18]。它仍然是可配置的（例如通过命令行选项），但在shell中连接输入和输出的灵活性被削弱了。

1. Sanjay Ghemawat, Howard Gobioff, and Shun-Tak
      Leung: “[The Google File System](http://research.google.com/archive/gfs-sosp2003.pdf),”
      at *19th ACM Symposium on Operating Systems Principles* (SOSP), October 2003.
      [doi:10.1145/945445.945450](http://dx.doi.org/10.1145/945445.945450)

      > Unix工具使用stdin和stdout作为输入和输出，而MapReduce作业则是在分布式文件系统上读取和写入文件。在Hadoop的MapReduce实现中，该文件系统被称为HDFS（Hadoop分布式文件系统），是谷歌文件系统（GFS）的开源再实现[19]。

1. Michael Ovsiannikov, Silvius Rus, Damian Reeves, et al.:
      “[The Quantcast File System](http://db.disi.unitn.eu/pages/VLDBProgram/pdf/industry/p808-ovsiannikov.pdf),” *Proceedings of the VLDB Endowment*, volume 6, number 11, pages 1092–1101, August 2013.
      [doi:10.14778/2536222.2536234](http://dx.doi.org/10.14778/2536222.2536234)

1. “[OpenStack Swift 2.6.1 Developer Documentation](http://docs.openstack.org/developer/swift/),” OpenStack Foundation, *docs.openstack.org*, March 2016.

      > 除了HDFS，还有其他各种分布式文件系统，如GlusterFS和Quantcast文件系统（QFS）[20]。对象存储服务，如Amazon S3、Azure Blob Storage和OpenStack Swift[21]，在很多方面都很相似。iv 在本章中，我们将主要使用HDFS作为运行实例，但这些原则适用于任何分布式文件系统。

1. Zhe Zhang, Andrew Wang, Kai Zheng, et al.:
      “[Introduction to HDFS Erasure Coding in Apache Hadoop](https://blog.cloudera.com/introduction-to-hdfs-erasure-coding-in-apache-hadoop/),”
      *blog.cloudera.com*, September 23, 2015.

      > 为了容忍机器和磁盘的故障，文件块被复制到多台机器上。复制可能意味着简单地在多台机器上复制相同的数据，如第5章，或者是一种擦除编码方案，如Reed-Solomon码，它允许以低于完全复制的存储开销恢复丢失的数据[20, 22]。这些技术类似于RAID，它在连接到同一台机器的几个磁盘上提供冗余；不同的是，在分布式文件系统中，文件访问和复制是通过传统的数据中心网络完成的，不需要特殊硬件。

1. Peter Cnudde:
      “[Hadoop Turns 10](https://web.archive.org/web/20190119112713/https://yahoohadoop.tumblr.com/post/138739227316/hadoop-turns-10),”
      *yahoohadoop.tumblr.com*, February 5, 2016.

1. Eric Baldeschwieler:
      “[Thinking About the HDFS vs. Other Storage Technologies](https://web.archive.org/web/20190529215115/http://hortonworks.com/blog/thinking-about-the-hdfs-vs-other-storage-technologies/),”
      *hortonworks.com*, July 25, 2012.

      > HDFS具有良好的扩展性：在撰写本文时，最大的HDFS部署在数万台机器上运行，综合存储容量达数百PB[23]。这样的大规模是可行的，因为使用商品硬件和开源软件，在HDFS上存储和访问数据的成本比专用存储设备上的同等容量要低得多[24]。

1. Brendan Gregg:
      “[Manta: Unix Meets Map Reduce](http://dtrace.org/blogs/brendan/2013/06/25/manta-unix-meets-map-reduce/),” *dtrace.org*, June 25, 2013.

1. Tom White: *Hadoop: The Definitive Guide*,
      4th edition. O'Reilly Media, 2015. ISBN: 978-1-491-90163-2

1. Jim N. Gray:
      “[Distributed Computing Economics](http://arxiv.org/pdf/cs/0403019.pdf),” Microsoft
      Research Tech Report MSR-TR-2003-24, March 2003.

      > 每个输入文件通常有数百兆字节大小。MapReduce调度器（图中未显示）试图在存储输入文件副本的一台机器上运行每个映射器，只要该机器有足够的空闲内存和CPU资源来运行映射任务[26]。这个原则被称为把计算放在数据附近[27]：它节省了在网络上复制输入文件，减少了网络负载，增加了本地性。

1. Márton Trencséni:
      “[Luigi vs Airflow vs Pinball](http://bytepawn.com/luigi-airflow-pinball.html),”
      *bytepawn.com*, February 6, 2016.

      > 一个批处理作业的输出只有在该作业成功完成后才被认为是有效的（MapReduce会丢弃失败作业的部分输出）。因此，工作流中的一个作业只有在前面的作业--即产生其输入目录的作业--成功完成后才能开始。为了处理作业执行之间的这些依赖关系，已经开发了各种Hadoop的工作流调度器，包括Oozie、Azkaban、Luigi、Airflow和Pinball [28]。

1. Roshan Sumbaly, Jay Kreps, and Sam Shah:
      “[The 'Big Data' Ecosystem at LinkedIn](http://www.slideshare.net/s_shah/the-big-data-ecosystem-at-linkedin-23512853),” at *ACM International Conference on Management of Data*
      (SIGMOD), July 2013.
      [doi:10.1145/2463676.2463707](http://dx.doi.org/10.1145/2463676.2463707)

      > 这些调度器也有管理功能，在维护大量的批处理作业集合时很有用。在构建推荐系统时，由50到100个MapReduce作业组成的工作流是很常见的[29]，在一个大型组织中，许多不同的团队可能会运行不同的作业，并互相读取对方的输出。工具支持对于管理这种复杂的数据流是很重要的。

1. Alan F. Gates, Olga Natkovich, Shubham Chopra, et al.:
      “[Building a High-Level Dataflow System on Top of Map-Reduce: The Pig Experience](http://www.vldb.org/pvldb/vol2/vldb09-1074.pdf),”
      at *35th International Conference on Very Large Data Bases* (VLDB), August 2009.

1. Ashish Thusoo, Joydeep Sen Sarma, Namit Jain, et al.:
      “[Hive – A Petabyte Scale Data Warehouse Using Hadoop](http://i.stanford.edu/~ragho/hive-icde2010.pdf),” at *26th IEEE International Conference on Data Engineering* (ICDE), March 2010.
      [doi:10.1109/ICDE.2010.5447738](http://dx.doi.org/10.1109/ICDE.2010.5447738)

1. “[Cascading 3.0 User Guide](http://docs.cascading.org/cascading/3.0/userguide/),” Concurrent, Inc., *docs.cascading.org*, January 2016.

1. “[Apache Crunch User Guide](https://crunch.apache.org/user-guide.html),” Apache Software Foundation, *crunch.apache.org*.

1. Craig Chambers, Ashish Raniwala, Frances
      Perry, et al.: “[FlumeJava: Easy, Efficient Data-Parallel Pipelines](https://research.google.com/pubs/archive/35650.pdf),” at *31st ACM SIGPLAN Conference on Programming Language
      Design and Implementation* (PLDI), June 2010.
      [doi:10.1145/1806596.1806638](http://dx.doi.org/10.1145/1806596.1806638)

      > Hadoop的各种高级工具，如Pig[30]、Hive[31]、Cascading[32]、Crunch[33]和FlumeJava[34]，也设置了多个MapReduce阶段的工作流程，并自动将其适当地连在一起。

1. Jay Kreps:
      “[Why Local State is a Fundamental Primitive in Stream Processing](https://www.oreilly.com/ideas/why-local-state-is-a-fundamental-primitive-in-stream-processing),” *oreilly.com*, July 31, 2014.

      > 这种连接的最简单的实现是逐一检查活动事件，并为它遇到的每个用户ID查询用户数据库（在远程服务器上）。这是有可能的，但它很可能会有很差的性能：处理量会受到到数据库服务器的往返时间的限制，本地缓存的有效性在很大程度上取决于数据的分布，而且并行运行大量的查询很容易使数据库不堪重负[35]。

1. Martin Kleppmann:
      “[Rethinking Caching in Web Apps](http://martin.kleppmann.com/2012/10/01/rethinking-caching-in-web-apps.html),” *martin.kleppmann.com*, October 1, 2012.

1. Mark Grover, Ted Malaska, Jonathan
      Seidman, and Gwen Shapira: *[Hadoop Application Architectures](http://shop.oreilly.com/product/0636920033196.do)*. O'Reilly Media, 2015. ISBN: 978-1-491-90004-8

      > 分组的另一个常见用途是整理一个特定用户会话的所有活动事件，以找出用户采取的行动序列--这一过程被称为会话化[37]。例如，这样的分析可以用来计算出显示新版网站的用户是否比显示旧版网站的用户更有可能进行购买（A/B测试），或者计算出某些营销活动是否值得。

1. Philippe Ajoux, Nathan Bronson,
      Sanjeev Kumar, et al.:
      “[Challenges to Adopting Stronger Consistency at Scale](https://www.usenix.org/system/files/conference/hotos15/hotos15-paper-ajoux.pdf),” at *15th USENIX Workshop on Hot Topics in
      Operating Systems* (HotOS), May 2015.

      > 如果有非常多的数据与单个键相关，"将所有具有相同键的记录带到同一个地方 "的模式就会被打破。例如，在一个社交网络中，大多数用户可能与几百个人有联系，但少数名人可能有几百万的追随者。这种不成比例的活跃的数据库记录被称为linchpin对象[38]或热键。

1. Sriranjan Manjunath:
      “[Skewed Join](https://wiki.apache.org/pig/PigSkewedJoinSpec),” *wiki.apache.org*,
      2009.

      > 如果一个连接输入有热键，你可以用一些算法来补偿。例如，Pig中的倾斜连接方法首先运行一个采样工作，以确定哪些键是热键[39]。当执行实际的连接时，映射器将与热键有关的任何记录发送到随机选择的几个还原器中的一个（与传统的MapReduce相反，它根据键的哈希值确定地选择一个还原器）。对于连接的其他输入，与热键有关的记录需要被复制到所有处理该键的还原器[40]。

1. David J. DeWitt, Jeffrey F. Naughton, Donovan A.
      Schneider, and S. Seshadri: “[Practical Skew Handling in Parallel Joins](http://www.vldb.org/conf/1992/P027.PDF),” at *18th International Conference on Very Large Data Bases* (VLDB), August 1992.

      > 如果一个连接输入有热键，你可以用一些算法来补偿。例如，Pig中的倾斜连接方法首先运行一个采样工作，以确定哪些键是热键[39]。当执行实际的连接时，映射器将与热键有关的任何记录发送到随机选择的几个还原器中的一个（与传统的MapReduce相反，它根据键的哈希值确定地选择一个还原器）。对于连接的其他输入，与热键有关的记录需要被复制到所有处理该键的还原器[40]。
      >
      > 

1. Marcel Kornacker, Alexander Behm, Victor
      Bittorf, et al.: “[Impala: A Modern, Open-Source SQL Engine for Hadoop](http://pandis.net/resources/cidr15impala.pdf),” at *7th Biennial Conference on Innovative Data Systems
      Research* (CIDR), January 2015.

      > 这种简单而有效的算法被称为广播式哈希连接：广播这个词反映了这样一个事实：大输入的一个分区的每个映射器都会读取小输入的全部内容（所以小输入实际上是 "广播 "给大输入的所有分区），而哈希这个词反映了它对哈希表的使用。这种连接方法被Pig（以 "复制式连接 "的名义）、Hive（"MapJoin"）、Cascading和Crunch支持。它也被用于数据仓库查询引擎，如Impala[41]。
      >
      > 

1. Matthieu Monsch:
      “[Open-Sourcing PalDB, a Lightweight Companion for Storing Side Data](https://engineering.linkedin.com/blog/2015/10/open-sourcing-paldb--a-lightweight-companion-for-storing-side-da),” *engineering.linkedin.com*, October 26, 2015.

      > 与其将小连接输入加载到内存哈希表中，另一种方法是将小连接输入存储在本地磁盘上的只读索引中[42]。这个索引的常用部分将保留在操作系统的页面缓存中，因此这种方法可以提供几乎与内存哈希表一样快的随机访问查询，但实际上不需要将数据集装入内存。

1. Daniel Peng and Frank Dabek:
      “[Large-Scale Incremental Processing Using Distributed Transactions and Notifications](https://www.usenix.org/legacy/event/osdi10/tech/full_papers/Peng.pdf),” at *9th USENIX
      conference on Operating Systems Design and Implementation* (OSDI), October 2010.

      > 谷歌最初使用MapReduce是为了给其搜索引擎建立索引，这是以5到10个MapReduce作业的工作流程来实现的[1]。尽管Google后来不再将MapReduce用于这一目的[43]，但如果你通过建立搜索索引的角度来看待MapReduce，这有助于理解MapReduce。(即使在今天，Hadoop MapReduce仍然是为Lucene/Solr建立索引的好方法[44]）。

1. “["Cloudera Search User Guide,"](http://www.cloudera.com/documentation/cdh/5-1-x/Search/Cloudera-Search-User-Guide/Cloudera-Search-User-Guide.html) Cloudera, Inc., September 2015.

      > 谷歌最初使用MapReduce是为了给其搜索引擎建立索引，这是以5到10个MapReduce作业的工作流程来实现的[1]。尽管Google后来不再将MapReduce用于这一目的[43]，但如果你通过建立搜索索引的角度来看待MapReduce，这有助于理解MapReduce。(即使在今天，Hadoop MapReduce仍然是为Lucene/Solr建立索引的好方法[44]）。
      >
      > 

1. Lili Wu, Sam Shah, Sean Choi, et al.:
      “[The Browsemaps: Collaborative Filtering at LinkedIn](http://ceur-ws.org/Vol-1271/Paper3.pdf),”
      at *6th Workshop on Recommender Systems and the Social Web* (RSWeb), October 2014.

      > 这些批处理作业的输出通常是某种数据库：例如，一个可以通过用户ID查询以获得该用户的建议朋友的数据库，或者一个可以通过产品ID查询以获得相关产品列表的数据库[45]。

1. Roshan Sumbaly, Jay Kreps, Lei Gao, et al.:
      “[Serving Large-Scale Batch Computed Data with Project Voldemort](http://static.usenix.org/events/fast12/tech/full_papers/Sumbaly.pdf),” at *10th USENIX Conference on File and Storage
      Technologies* (FAST), February 2012.

1. Varun Sharma:
      “[Open-Sourcing Terrapin: A Serving System for Batch Generated Data](https://web.archive.org/web/20170215032514/https://engineering.pinterest.com/blog/open-sourcing-terrapin-serving-system-batch-generated-data-0),”
      *engineering.pinterest.com*, September 14, 2015.

1. Nathan Marz:
      “[ElephantDB](http://www.slideshare.net/nathanmarz/elephantdb),” *slideshare.net*, May 30, 2011.

      > 

1. Jean-Daniel (JD) Cryans:
      “[How-to: Use HBase Bulk Loading, and Why](https://blog.cloudera.com/how-to-use-hbase-bulk-loading-and-why/),”
      *blog.cloudera.com*, September 27, 2013.

      > 一个更好的解决方案是在批处理作业中建立一个全新的数据库，并将其作为文件写入分布式文件系统中作业的输出目录中，就像上一节中的搜索索引。这些数据文件一旦写入就不可改变，并且可以批量加载到处理只读查询的服务器中。各种键值存储支持在MapReduce作业中建立数据库文件，包括Voldemort[46]、Terrapin[47]、ElephantDB[48]和HBase批量加载[49]。
      >
      > 

1. Nathan Marz:
      “[How to Beat the CAP   Theorem](http://nathanmarz.com/blog/how-to-beat-the-cap-theorem.html),” *nathanmarz.com*, October 13, 2011.

      >  如果你在代码中引入了一个错误，输出是错误的或损坏的，你可以简单地回滚到以前的代码版本并重新运行作业，输出将再次正确。或者，更简单的是，你可以把旧的输出放在不同的目录中，并简单地切换回它。有读写事务的数据库不具备这种特性：如果你部署了有问题的代码，向数据库写了坏的数据，那么回滚代码对修复数据库中的数据毫无帮助。(能够从有缺陷的代码中恢复的想法被称为人类的容错性[50]）。 
      >
      > 

1. Molly Bartlett Dishman and Martin Fowler:
      “[Agile   Architecture](http://conferences.oreilly.com/software-architecture/sa2015/public/schedule/detail/40388),” at *O'Reilly Software Architecture Conference*, March 2015.

      > 由于这种回滚的便利性，功能开发可以比在一个错误可能意味着不可逆转的环境下更快地进行。这种最小化不可逆转性的原则对敏捷软件开发是有益的[51]。
      >
      > 

1. David J. DeWitt and Jim N. Gray:
      “[Parallel Database Systems: The Future of High Performance Database Systems](http://www.cs.cmu.edu/~pavlo/courses/fall2013/static/papers/dewittgray92.pdf),”
      *Communications of the ACM*, volume 35, number 6, pages 85–98, June 1992.
      [doi:10.1145/129888.129894](http://dx.doi.org/10.1145/129888.129894)

      > 当MapReduce论文[1]发表时，从某种意义上说，它一点也不新鲜。我们在最后几节中讨论的所有处理和并行连接算法，在十多年前就已经在所谓的大规模并行处理（MPP）数据库中实现了[3, 40]。例如，Gamma数据库机器、Teradata和Tandem NonStop SQL是这个领域的先驱[52]。
      >
      > 

1. Jay Kreps:
      “[But the multi-tenancy thing is actually really really hard](https://twitter.com/jaykreps/status/528235702480142336),” tweetstorm, *twitter.com*, October 31, 2014.

      > 直截了当地说，Hadoop开启了将数据不分青红皂白地倾倒到HDFS中的可能性，后来才想出如何进一步处理它[53]。相比之下，MPP数据库通常需要在将数据导入数据库的专有存储格式之前对数据和查询模式进行仔细的前期建模。
      >
      > 

1. Jeffrey Cohen, Brian Dolan, Mark Dunlap, et al.:
      “[MAD Skills: New Analysis Practices for Big Data](http://www.vldb.org/pvldb/vol2/vldb09-219.pdf),”
      *Proceedings of the VLDB Endowment*, volume 2, number 2, pages 1481–1492, August 2009.
      [doi:10.14778/1687553.1687576](http://dx.doi.org/10.14778/1687553.1687576)

      > 从纯粹主义者的角度来看，这种仔细的建模和导入似乎是可取的，因为这意味着数据库的用户有更好的质量的数据来工作。然而，在实践中，似乎仅仅是快速提供数据--即使它是一个古怪的、难以使用的原始格式--往往比试图预先决定理想的数据模型更有价值[54]。
      >
      > 

1. Ignacio
      Terrizzano, Peter Schwarz, Mary Roth, and John E. Colino:
      “[Data Wrangling: The Challenging Journey from the Wild to the Lake](http://cidrdb.org/cidr2015/Papers/CIDR15_Paper2.pdf),” at *7th Biennial Conference on Innovative Data Systems
      Research* (CIDR), January 2015.

      > 这个想法类似于数据仓库（见 "数据仓库"）：简单地将一个大型组织的各个部分的数据汇集到一个地方是很有价值的，因为它可以在以前不相干的数据集之间进行连接。MPP数据库所要求的仔细的模式设计减缓了这种集中的数据收集；收集原始形式的数据，并在之后担心模式设计，可以加快数据收集的速度（这个概念有时被称为 "数据湖 "或 "企业数据中心"[55]）。

1. Paige Roberts:
      “[To Schema on Read or to Schema on Write, That Is the Hadoop Data Lake Question](http://adaptivesystemsinc.com/blog/to-schema-on-read-or-to-schema-on-write-that-is-the-hadoop-data-lake-question/),” *adaptivesystemsinc.com*, July 2, 2015.

      > 

1. Bobby Johnson and Joseph Adler:
      “[The Sushi Principle: Raw Data Is Better](https://conferences.oreilly.com/strata/big-data-conference-ca-2015/public/schedule/detail/38737),”
      at *Strata+Hadoop World*, February 2015.

      > 不加区分的数据转储转移了解释数据的负担：不是强迫数据集的生产者将其带入一个标准化的格式，而是将数据的解释变成了消费者的问题（schema-on-read方法[56]；见 "文档模型的schema灵活性"）。如果生产者和消费者是具有不同优先级的不同团队，这可能是一个优势。甚至可能没有一个理想的数据模型，而是有适合不同目的的对数据的不同看法。简单地以原始形式倾倒数据，就可以进行一些这样的转换。这种方法被称为寿司原则："原始数据更好"[57]。
      >
      > 

1. Vinod Kumar Vavilapalli, Arun C. Murthy, Chris Douglas, et al.:
      “[Apache Hadoop YARN: Yet Another Resource Negotiator](http://www.socc2013.org/home/program/a5-vavilapalli.pdf),” at *4th ACM Symposium on Cloud Computing* (SoCC), October 2013.
      [doi:10.1145/2523616.2523633](http://dx.doi.org/10.1145/2523616.2523633)

      > 后来，人们发现MapReduce的局限性太大，对某些类型的处理来说表现太差，所以在Hadoop的基础上开发了各种其他的处理模型（我们将在 "超越MapReduce "中看到其中一些模型）。有两种处理模式，即SQL和MapReduce，是不够的：甚至需要更多不同的模式 由于Hadoop平台的开放性，实现一系列的方法是可行的，这在单一的MPP数据库的范围内是不可能的[58]。
      >
      > 

1. Abhishek Verma, Luis Pedrosa, Madhukar Korupolu, et al.:
      “[Large-Scale Cluster Management at Google with Borg](http://research.google.com/pubs/pub43438.html),” at *10th European Conference on Computer Systems* (EuroSys), April 2015.
      [doi:10.1145/2741948.2741964](http://dx.doi.org/10.1145/2741948.2741964)

      > 为了理解MapReduce节约使用内存和任务级恢复的原因，看看MapReduce最初设计的环境是很有帮助的。谷歌拥有混合使用的数据中心，其中在线生产服务和离线批处理作业在同一台机器上运行。每个任务都有一个资源分配（CPU核心、内存、磁盘空间等），并使用容器强制执行。每个任务也有一个优先级，如果一个优先级较高的任务需要更多的资源，同一台机器上优先级较低的任务可以被终止（抢占），以释放资源。优先权也决定了计算资源的定价：团队必须为他们使用的资源付费，优先权较高的进程花费更多[59]。
      >
      > 

1. Malte Schwarzkopf:
      “[The Evolution of Cluster Scheduler Architectures](http://www.firmament.io/blog/scheduler-architectures.html),” *firmament.io*, March 9, 2016.

      > 在开源集群调度器中，抢占的应用不太广泛。YARN的CapacityScheduler支持抢占，以平衡不同队列的资源分配[58]，但在撰写本文时，YARN、Mesos或Kubernetes都不支持一般的优先抢占[60]。在一个任务不那么经常被终止的环境中，MapReduce的设计决策就不那么合理了。在下一节中，我们将看一下MapReduce的一些替代方案，这些方案做出了不同的设计决定。

1. Matei Zaharia, Mosharaf Chowdhury, Tathagata Das, et al.:
      “[Resilient Distributed Datasets: A Fault-Tolerant Abstraction for In-Memory Cluster Computing](https://www.usenix.org/system/files/conference/nsdi12/nsdi12-final138.pdf),” at *9th
      USENIX Symposium on Networked Systems Design and Implementation* (NSDI), April 2012.

1. Holden Karau, Andy Konwinski, Patrick Wendell, and Matei
      Zaharia: *Learning Spark*. O'Reilly Media, 2015. ISBN: 978-1-449-35904-1

1. Bikas Saha and Hitesh Shah:
      “[Apache Tez: Accelerating Hadoop Query Processing](http://www.slideshare.net/Hadoop_Summit/w-1205phall1saha),” at *Hadoop Summit*, June 2014.

1. Bikas Saha, Hitesh Shah, Siddharth Seth, et al.:
      “[Apache Tez: A Unifying Framework for Modeling and Building Data Processing Applications](http://home.cse.ust.hk/~weiwa/teaching/Fall15-COMP6611B/reading_list/Tez.pdf),” at *ACM
      International Conference on Management of Data* (SIGMOD), June 2015.
      [doi:10.1145/2723372.2742790](http://dx.doi.org/10.1145/2723372.2742790)

1. Kostas Tzoumas:
      “[Apache Flink: API, Runtime, and Project Roadmap](http://www.slideshare.net/KostasTzoumas/apache-flink-api-runtime-and-project-roadmap),” *slideshare.net*, January 14, 2015.

      > 

1. Alexander Alexandrov, Rico Bergmann, Stephan Ewen, et al.:
      “[The Stratosphere Platform for Big Data Analytics](https://ssc.io/pdf/2014-VLDBJ_Stratosphere_Overview.pdf),” *The VLDB Journal*, volume 23, number 6, pages 939–964, May 2014.
      [doi:10.1007/s00778-014-0357-y](http://dx.doi.org/10.1007/s00778-014-0357-y)

      > 为了解决MapReduce的这些问题，人们开发了几个新的分布式批处理计算的执行引擎，其中最著名的是Spark[61, 62]、Tez[63, 64]和Flink[65, 66]。它们的设计方式有各种不同，但它们有一个共同点：它们将整个工作流作为一个作业来处理，而不是将其分解成独立的子作业。

1. Michael Isard, Mihai Budiu, Yuan Yu, et al.:
      “[Dryad: Distributed Data-Parallel Programs from Sequential Building Blocks](https://www.microsoft.com/en-us/research/publication/dryad-distributed-data-parallel-programs-from-sequential-building-blocks/),” at *European Conference on Computer
      Systems* (EuroSys), March 2007.
      [doi:10.1145/1272996.1273005](http://dx.doi.org/10.1145/1272996.1273005)

      > 

1. Daniel Warneke and Odej Kao:
      “[Nephele: Efficient Parallel Data Processing in the Cloud](https://stratosphere2.dima.tu-berlin.de/assets/papers/Nephele_09.pdf),” at *2nd Workshop on Many-Task Computing on Grids and
      Supercomputers* (MTAGS), November 2009.
      [doi:10.1145/1646468.1646476](http://dx.doi.org/10.1145/1646468.1646476)

      > 这种处理引擎的风格是基于Dryad[67]和Nephele[68]等研究系统，与MapReduce模型相比，它有几个优点。
      >
      > 

1. Lawrence Page, Sergey Brin, Rajeev Motwani, and Terry Winograd:
      “[The PageRank Citation Ranking: Bringing Order to the Web](http://ilpubs.stanford.edu:8090/422/),”
      Stanford InfoLab Technical Report 422, 1999.

      > 在批处理的背景下看图也很有意思，其目的是对整个图进行某种离线处理或分析。这种需求经常出现在机器学习应用中，比如推荐引擎，或者排名系统中。例如，最著名的图分析算法之一是PageRank[69]，它试图根据其他网页对它的链接来估计一个网页的受欢迎程度。它被用作决定网络搜索引擎呈现其结果的顺序的公式的一部分。

1. Leslie G. Valiant:
      “[A Bridging Model for Parallel Computation](http://dl.acm.org/citation.cfm?id=79181),”
      *Communications of the ACM*, volume 33, number 8, pages 103–111, August 1990.
      [doi:10.1145/79173.79181](http://dx.doi.org/10.1145/79173.79181)

1. Stephan Ewen, Kostas Tzoumas, Moritz Kaufmann, and Volker Markl:
      “[Spinning Fast Iterative Data Flows](http://vldb.org/pvldb/vol5/p1268_stephanewen_vldb2012.pdf),” *Proceedings of the VLDB Endowment*, volume 5, number 11, pages 1268-1279, July 2012.
      [doi:10.14778/2350229.2350245](http://dx.doi.org/10.14778/2350229.2350245)

1. Grzegorz Malewicz, Matthew H.
      Austern, Aart J. C. Bik, et al.: “[Pregel: A System for Large-Scale Graph Processing](https://kowshik.github.io/JPregel/pregel_paper.pdf),” at *ACM International Conference on Management of
      Data* (SIGMOD), June 2010.
      [doi:10.1145/1807167.1807184](http://dx.doi.org/10.1145/1807167.1807184)

      > 作为对批量处理图的优化，批量同步并行（BSP）计算模型[70]已经变得很流行。其中，它由Apache Giraph[37]、Spark的GraphX API和Flink的Gelly API[71]实现。它也被称为Pregel模型，因为谷歌的Pregel论文普及了这种处理图的方法[72]。

1. Frank McSherry, Michael Isard, and Derek G. Murray:
      “[Scalability! But at What COST?](http://www.frankmcsherry.org/assets/COST.pdf),” at
      *15th USENIX Workshop on Hot Topics in Operating Systems* (HotOS), May 2015.

1. Ionel Gog, Malte Schwarzkopf, Natacha Crooks, et al.:
      “[Musketeer: All for One, One for All in Data Processing Systems](http://www.cl.cam.ac.uk/research/srg/netos/camsas/pubs/eurosys15-musketeer.pdf),” at *10th European Conference on
      Computer Systems* (EuroSys), April 2015.
      [doi:10.1145/2741948.2741968](http://dx.doi.org/10.1145/2741948.2741968)

1. Aapo Kyrola, Guy Blelloch, and Carlos Guestrin:
      “[GraphChi: Large-Scale Graph Computation on Just a PC](https://www.usenix.org/system/files/conference/osdi12/osdi12-final-126.pdf),” at *10th USENIX Symposium on Operating Systems
      Design and Implementation* (OSDI), October 2012.

1. Andrew Lenharth, Donald Nguyen, and Keshav Pingali:
      “[Parallel Graph Analytics](http://cacm.acm.org/magazines/2016/5/201591-parallel-graph-analytics/fulltext),” *Communications of the ACM*, volume 59, number 5, pages 78–87, May
      2016. [doi:10.1145/2901919](http://dx.doi.org/10.1145/2901919)

      > 出于这个原因，如果你的图可以装在一台计算机的内存中，那么很可能单机（甚至可能是单线程）的算法会优于分布式批处理[73, 74]。即使图比内存大，它也可以装在一台计算机的磁盘上，使用GraphChi这样的框架进行单机处理是一个可行的选择[75]。如果图太大，不能放在单机上，那么像Pregel这样的分布式方法是不可避免的；有效地将图算法并行化是一个正在研究的领域[76]。

1. Fabian Hüske:
      “[Peeking into Apache Flink's Engine Room](http://flink.apache.org/news/2015/03/13/peeking-into-Apache-Flinks-Engine-Room.html),” *flink.apache.org*, March 13, 2015.

1. Mostafa Mokhtar:
      “[Hive 0.14 Cost Based Optimizer (CBO) Technical Overview](https://web.archive.org/web/20170607112708/http://hortonworks.com/blog/hive-0-14-cost-based-optimizer-cbo-technical-overview/),”
      *hortonworks.com*, March 2, 2015.

1. Michael Armbrust, Reynold S Xin, Cheng Lian, et al.:
      “[Spark SQL: Relational Data Processing in Spark](http://people.csail.mit.edu/matei/papers/2015/sigmod_spark_sql.pdf),” at *ACM International Conference on Management of Data* (SIGMOD), June 2015.
      [doi:10.1145/2723372.2742797](http://dx.doi.org/10.1145/2723372.2742797)

      > 与写出执行连接的代码相比，将连接指定为关系运算符的一个好处是，框架可以分析连接输入的属性，并自动决定上述的连接算法中哪一种最适合手头的任务。Hive、Spark和Flink有基于成本的查询优化器，可以做到这一点，甚至可以改变连接的顺序，使中间状态的数量最小化[66, 77, 78, 79]。

1. Daniel Blazevski:
      “[Planting Quadtrees for Apache Flink](http://insightdataengineering.com/blog/flink-knn/),” *insightdataengineering.com*, March 25, 2016.

1. Tom White:
      “[Genome Analysis Toolkit: Now Using Apache Spark for Data Processing](https://web.archive.org/web/20190215132904/http://blog.cloudera.com/blog/2016/04/genome-analysis-toolkit-now-using-apache-spark-for-data-processing/),”
      *blog.cloudera.com*, April 6, 2016.

      > 同样有用的是空间算法，如k-nearest neighbors[80]，它在一些多维空间中搜索与给定项目接近的项目--一种相似性搜索。近似搜索对基因组分析算法也很重要，它需要找到相似但不相同的字符串[81]。
