Designing Data-Intensive Applications
=====================================

Chapter 3 Storage and Retrieval
--------------------

1. Alfred V. Aho, John E. Hopcroft, and Jeffrey D. Ullman:
    *Data Structures and Algorithms*. Addison-Wesley, 1983. ISBN: 978-0-201-00023-8

1. Thomas H. Cormen, Charles E. Leiserson, Ronald L. Rivest, and
    Clifford Stein: *Introduction to Algorithms*, 3rd edition. MIT Press, 2009.
    ISBN: 978-0-262-53305-8

    > 哈希索引
    >
    > ……许多算法资料中都介绍过 hash map[1，2]，所以这里不再详细介绍它们工作的细节

1. Justin Sheehy and David Smith:
    “[Bitcask: A Log-Structured Hash Table for Fast Key/Value Data](https://riak.com/assets/bitcask-intro.pdf),” Basho Technologies, April 2010.

    > 哈希索引
    >
    > ……最简单的索引策略就是，保存内存中的hash map，把每个键一一映射到数据文件中特定的字节偏移量，这样就可以找到每个值的位置……事实上，这就是 Bitcast（Riak 中的默认存储引擎）所采用的核心做法

1. Yinan Li, Bingsheng He, Robin Jun Yang, et al.:
      “[Tree Indexing on Solid State Drives](http://www.vldb.org/pvldb/vldb2010/papers/R106.pdf),”
      *Proceedings of the VLDB Endowment*, volume 3, number 1, pages 1195–1206,
      September 2010.

      > 哈希索引
      >
      > ……结果证明追加式的设计非常不错，原因有以下几个……在某种程度上顺序写入在基于闪存的固态硬盘上也是适合的

1. Goetz Graefe:
      “[Modern B-Tree Techniques](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.219.7269&rep=rep1&type=pdf),”
      *Foundations and Trends in Databases*, volume 3, number 4, pages 203–402, August 2011.
      [doi:10.1561/1900000028](http://dx.doi.org/10.1561/1900000028)

      > 哈希索引
      >
      > ……哈希索引也有其局限性……原则上，可以在磁盘上维护hash map，但不幸的是，很难使磁盘上的hasp map 表现良好。……并且哈希冲突时需要复杂的处理逻辑

1. Jeffrey Dean and Sanjay Ghemawat:
    “[LevelDB Implementation Notes](https://github.com/google/leveldb/blob/master/doc/impl.md),”
    *github.com*.

1. Dhruba Borthakur:
    “[The History of RocksDB](https://rocksdb.blogspot.com/2013/11/the-history-of-rocksdb.html),”
    *rocksdb.blogspot.com*, November 24, 2013.

    >从 SSTables 到 LSM-Tree
    >
    >以上描述的算法本质上正是 LevelDB[6] 和 RocksDB[7] 所使用的

1. Matteo Bertozzi:
    “[Apache HBase I/O – HFile](https://blog.cloudera.com/apache-hbase-i-o-hfile/),” *blog.cloudera.com*, June 29, 2012.

1. Fay Chang, Jeffrey Dean, Sanjay Ghemawat, et al.:
    “[Bigtable: A Distributed Storage System for Structured Data](https://research.google/pubs/pub27898/),” at *7th USENIX Symposium on Operating System Design and
    Implementation* (OSDI), November 2006.

    > 从 SSTables 到 LSM-Tree
    >
    > ……类似的存储引擎还被用于 Cassandra 和 Hbase[8]，都受到 Google 的 Bigtable[9] 论文的启发

1. Patrick
    O'Neil, Edward Cheng, Dieter Gawlick, and Elizabeth O'Neil:
    “[The Log-Structured Merge-Tree (LSM-Tree)](http://www.cs.umb.edu/~poneil/lsmtree.pdf),”
    *Acta Informatica*, volume 33, number 4, pages 351–385, June 1996.
    [doi:10.1007/s002360050048](http://dx.doi.org/10.1007/s002360050048)

1. Mendel Rosenblum and John K. Ousterhout:
     “[The Design and Implementation of a Log-Structured File System](http://research.cs.wisc.edu/areas/os/Qual/papers/lfs.pdf),”
     *ACM Transactions on Computer Systems*, volume 10, number 1, pages 26–52, February 1992.
     [doi:10.1145/146941.146943](http://dx.doi.org/10.1145/146941.146943)

     > 从 SSTables 到 LSM-Tree
     >
     > ……最初这个索引结构由 Patrick O'Neil 等人以日志结构的合并树（Log-structured Merge-Tree，或 LSM-Tree）[10] 命名，它建立在更早期的日志结构文件系统之上[11]

1. Adrien Grand:
     “[What Is in a Lucene Index?](http://www.slideshare.net/lucenerevolution/what-is-inaluceneagrandfinal),” at *Lucene/Solr Revolution*, November 14, 2013.

1. Deepak Kandepet:
     “[Hacking Lucene—The Index Format](https://web.archive.org/web/20160316190830/http://hackerlabs.github.io/blog/2011/10/01/hacking-lucene-the-index-format/index.html),” *hackerlabs.github.io*, October 1, 2011.

     > 从 SSTables 到 LSM-Tree
     >
     > ……Lucene 是 Elasticsearch 和 Solr 等全文搜索系统所使用的索引引擎，它采用了类似的方法来保存其词典

1. Michael McCandless:
     “[Visualizing Lucene's Segment Merges](http://blog.mikemccandless.com/2011/02/visualizing-lucenes-segment-merges.html),” *blog.mikemccandless.com*, February 11, 2011.

     > 从 SSTables 到 LSM-Tree
     >
     > ……在 Lucene 中，从词条到 posting list 的映射关系保存在类 SSTable 的排序文件中，这些文件可以根据需要在后台合并

1. Burton H. Bloom:
     “[Space/Time Trade-offs in Hash Coding with Allowable Errors](https://people.cs.umass.edu/~emery/classes/cmpsci691st/readings/Misc/p422-bloom.pdf),”
     *Communications of the ACM*, volume 13, number 7, pages 422–426, July 1970.
     [doi:10.1145/362686.362692](http://dx.doi.org/10.1145/362686.362692)

     > 性能优化
     >
     > ……查找不存在的键时，LSM-Tree 可能很慢……为了优化这种访问，存储引擎通常使用额外的布隆过滤器

1. “[Operating Cassandra: Compaction](https://cassandra.apache.org/doc/latest/operating/compaction.html),” Apache Cassandra Documentation v4.0, 2016.

     > 性能优化
     >
     > LevelDB 和 RocksDB 使用分层压缩，HBase 使用大小分级，Cassandra 则同时支持这两种压缩

1. Rudolf Bayer and Edward M. McCreight:
     “[Organization and Maintenance of Large Ordered Indices](http://www.dtic.mil/cgi-bin/GetTRDoc?AD=AD0712079),” Boeing Scientific Research Laboratories, Mathematical and Information Sciences
     Laboratory, report no. 20, July 1970.

1. Douglas Comer:
     “[The Ubiquitous B-Tree](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.96.6637&rep=rep1&type=pdf),” *ACM Computing Surveys*, volume 11, number 2, pages 121–137, June 1979.
     [doi:10.1145/356770.356776](http://dx.doi.org/10.1145/356770.356776)

     > B-trees
     >
     > B-trees 始见于 1970 年[17]，不到十年便被冠以“普遍存在”[18]，B-trees 经受了长久的时间考验

1. Emmanuel Goossaert:
     “[Coding for SSDs](http://codecapsule.com/2014/02/12/coding-for-ssds-part-1-introduction-and-table-of-contents/),” *codecapsule.com*, February 12, 2014.

1. C. Mohan and Frank Levine:
     “[ARIES/IM: An Efficient and High Concurrency Index Management Method Using Write-Ahead Logging](http://www.ics.uci.edu/~cs223/papers/p371-mohan.pdf),” at *ACM
     International Conference on Management of Data* (SIGMOD), June 1992.
     [doi:10.1145/130283.130338](http://dx.doi.org/10.1145/130283.130338)

     > B-trees
     >
     > ……预写日志（write-ahead log，WAL）……当数据库在崩溃后需要恢复时，该日志用于将 B-tree 恢复到最近一致的状态

1. Howard Chu:
      “[LDAP at Lightning Speed]( https://buildstuff14.sched.com/event/08a1a368e272eb599a52e08b4c3c779d),”
      at *Build Stuff '14*, November 2014.

      > 优化B-tree
      >
      > ……一些数据库（如 LMDB）不使用覆盖页和维护 WAL 来进行崩溃恢复，而是使用写时复制方案

1. Bradley C. Kuszmaul:
      “[A   Comparison of Fractal Trees to Log-Structured Merge (LSM) Trees](http://www.pandademo.com/wp-content/uploads/2017/12/A-Comparison-of-Fractal-Trees-to-Log-Structured-Merge-LSM-Trees.pdf),” *tokutek.com*,
      April 22, 2014.

      > 优化 B-tree
      >
      > ……B-tree 的变体如分形数，借鉴了一些日志结构的想法来减少磁盘寻道

1. Manos Athanassoulis, Michael S. Kester,
     Lukas M. Maas, et al.: “[Designing Access Methods: The RUM Conjecture](http://openproceedings.org/2016/conf/edbt/paper-12.pdf),” at *19th International Conference on Extending Database
     Technology* (EDBT), March 2016.
     [doi:10.5441/002/edbt.2016.42](http://dx.doi.org/10.5441/002/edbt.2016.42)

     > 对比B-tree 和 LSM-tree
     >
     > ……根据经验，LSM-tree 通常对于写入更快，而 B-tree 被认为对于读取更快

1. Peter Zaitsev:
     “[Innodb Double Write](https://www.percona.com/blog/2006/08/04/innodb-double-write/),”
     *percona.com*, August 4, 2006.

1. Tomas Vondra:
     “[On the Impact of Full-Page Writes](http://blog.2ndquadrant.com/on-the-impact-of-full-page-writes/),” *blog.2ndquadrant.com*, November 23, 2016.

     > LSM-tree 的优点
     >
     > ……一些存储引擎甚至覆盖相同的页两次，以避免在电源故障的情况下最终出现部分更新的页[24，25]

1. Mark Callaghan:
     “[The Advantages of an LSM vs a B-Tree](http://smalldatum.blogspot.co.uk/2016/01/summary-of-advantages-of-lsm-vs-b-tree.html),” *smalldatum.blogspot.co.uk*, January 19, 2016.

     > LSM-tree 的优点
     >
     > ……LSM-tree 通常能够承受比 B-tree 更高的写入吞吐量，部分是因为它们有时具有较低的写放大，部分原因是它们以顺序方式写入紧凑的 SSTable 文件，而不必充血树中的多个页

1. Mark Callaghan:
     “[Choosing Between Efficiency and Performance with RocksDB](https://codemesh.io/codemesh2016/mark-callaghan),” at *Code Mesh*, November 4, 2016.

     > LSM-tree 的优点
     >
     > ……由于 LSM-tree 不是面向页的，而且定期重写 SSTables 以消除碎片化，所以它们具有较低的存储开销，特别是在使用分层压缩时

1. Michi Mutsuzaki: “MySQL vs. LevelDB” &#91;URL inactive&#93;, August 2011.

     > LSM-tree 的缺点
     >
     > ……如果观察较高的百分位数，日志结构化存储引擎的查询响应时间有时会相当高，而 B-tree 的响应延迟则更具确定性

1. Benjamin Coverston,
     Jonathan Ellis, et al.: “[CASSANDRA-1608: Redesigned Compaction](https://issues.apache.org/jira/browse/CASSANDRA-1608), *issues.apache.org*, July 2011.

1. Igor Canadi, Siying Dong, and Mark Callaghan:
     “[RocksDB Tuning Guide](https://github.com/facebook/rocksdb/wiki/RocksDB-Tuning-Guide),”
     *github.com*, 2016.

     > LSM-tree 的缺点
     >
     > ……即使压缩不能跟上，基于 SSTable 的存储引擎也不会限制到来的写入速率，因此需要额外的监控措施来及时发现这种情况[29，30]

1. [*MySQL 5.7 Reference Manual*](http://dev.mysql.com/doc/refman/5.7/en/index.html).
     Oracle, 2014.

     > 在索引中存储值
     >
     > ……InnoDB 存储引擎中，表的主键始终是聚集索引，二级索引引用主键

1. [*Books Online for SQL Server 2012*](http://msdn.microsoft.com/en-us/library/ms130214.aspx).
     Microsoft, 2012.

     > 在索引中存储值
     >
     > ……在 SQL server 中，可以为每个表指定一个聚集索引

1. Joe Webb:
     “[Using Covering Indexes to Improve Query Performance](https://www.simple-talk.com/sql/learn-sql-server/using-covering-indexes-to-improve-query-performance/),” *simple-talk.com*, 29 September 2008.

     > 在索引中存储值
     >
     > ……聚集索引和非聚集索引之间有一种折中设计称为覆盖索引或包含列的索引，它在所有中保存一些表的列值

1. Frank Ramsak, Volker Markl, Robert Fenk, et al.:
     “[Integrating the UB-Tree into a Database System Kernel](http://www.vldb.org/conf/2000/P263.pdf),”
     at *26th International Conference on Very Large Data Bases* (VLDB), September 2000.

     > 多列索引
     >
     > ……一种选择是使用空格填充曲线将二维位置转换为单个数字，然后使用常规的B-tree 索引

1. The PostGIS Development Group:
     “[PostGIS 2.1.2dev Manual](http://postgis.net/docs/manual-2.1/),”
     *postgis.net*, 2014.

     > 多列索引
     >
     > ……PostGIS 使用 PostgreSQL的广义搜索树[35]实现了地理空间索引作为R树

1. Robert Escriva, Bernard Wong, and Emin Gün Sirer:
     “[HyperDex: A Distributed, Searchable Key-Value Store](http://www.cs.princeton.edu/courses/archive/fall13/cos518/papers/hyperdex.pdf),” at *ACM SIGCOMM Conference*, August 2012.
     [doi:10.1145/2377677.2377681](http://dx.doi.org/10.1145/2377677.2377681)

     > 多列索引
     >
     > ……二维索引可以通过时间戳和温度同时缩小查询范围。HyperDex 使用了这种技术

1. Michael McCandless:
     “[Lucene's FuzzyQuery Is 100 Times Faster in 4.0](http://blog.mikemccandless.com/2011/03/lucenes-fuzzyquery-is-100-times-faster.html),” *blog.mikemccandless.com*, March 24, 2011.

     > 

1. Steffen Heinz, Justin Zobel, and Hugh E. Williams:
     “[Burst Tries: A Fast, Efficient Data Structure for String Keys](http://citeseer.ist.psu.edu/viewdoc/summary?doi=10.1.1.18.3499),”
     *ACM Transactions on Information Systems*, volume 20, number 2, pages 192–223, April 2002.
     [doi:10.1145/506309.506312](http://dx.doi.org/10.1145/506309.506312)

     > 全文搜索和模糊索引
     >
     > ……在levelDB 中，这个内存中的索引是一些键的稀疏集合，但是在 Lucene 中，内存中的索引是键中的字符序列的有限状态自动机，类似字典树

1. Klaus U. Schulz and Stoyan Mihov:
     “[Fast String Correction with Levenshtein Automata](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.16.652),”
     *International Journal on Document Analysis and Recognition*,
     volume 5, number 1, pages 67–85, November 2002.
     [doi:10.1007/s10032-002-0082-8](http://dx.doi.org/10.1007/s10032-002-0082-8)

     > 全文搜索和模糊索引
     >
     > ……这个自动机可以转换成 Levenshtein 自动机，它支持在给定编辑距离内高效地搜索单词

1. Christopher D. Manning, Prabhakar Raghavan, and Hinrich Schütze:
     [*Introduction to Information Retrieval*](http://nlp.stanford.edu/IR-book/).
     Cambridge University Press, 2008. ISBN: 978-0-521-86571-5, available online at *nlp.stanford.edu/IR-book*

     > 全文搜索和模糊索引
     >
     > ……更多细节，请参阅相关信息检索教程

1. Michael Stonebraker, Samuel Madden, Daniel J. Abadi, et al.:
     “[The End of an Architectural Era (It’s Time for a Complete Rewrite)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.137.3697&rep=rep1&type=pdf),” at
     *33rd International Conference on Very Large Data Bases* (VLDB), September 2007.

1. “[VoltDB Technical Overview White Paper](https://www.voltdb.com/files/voltdb-technical-overview/),” VoltDB, 2014.

     > 在内存中保存所有内容
     >
     > ……诸如 VoltDB、MemSQL 和 Oracle TimesTen 的产品是具有关系模型的内存数据库，相关供应商声称通过移除所有与管理磁盘数据结构相关的开销，它们可以获得极大的性能提升

1. Stephen M. Rumble, Ankita Kejriwal, and John K. Ousterhout:
     “[Log-Structured Memory for DRAM-Based Storage](https://www.usenix.org/system/files/conference/fast14/fast14-paper_rumble.pdf),” at *12th USENIX Conference on File and Storage
     Technologies* (FAST), February 2014.

     > 在内存中保存所有内容
     >
     > ……RAMCloud 是一个开源的、具有持久性的内存 key-value 存储（对内存和磁盘上的数据使用日志结构）

1. Stavros Harizopoulos, Daniel J. Abadi,
     Samuel Madden, and Michael Stonebraker:
     “[OLTP Through the Looking Glass, and What We Found There](http://hstore.cs.brown.edu/papers/hstore-lookingglass.pdf),” at *ACM International Conference on Management of Data*
     (SIGMOD), June 2008.
     [doi:10.1145/1376616.1376713](http://dx.doi.org/10.1145/1376616.1376713)

     > 在内存中保存所有内容
     >
     > ……内存数据库可以更快，是因为它们避免使用写磁盘的格式对内存数据结构编码的开销

1. Justin DeBrabant, Andrew Pavlo, Stephen Tu, et al.:
     “[Anti-Caching: A New Approach to Database Management System Architecture](http://www.vldb.org/pvldb/vol6/p1942-debrabant.pdf),” *Proceedings of the VLDB Endowment*, volume 6,
     number 14, pages 1942–1953, September 2013.

     > 在内存中保存所有内容
     >
     > ……最近的研究表明，内存数据库架构可以扩展到支持远大于可用内存的数据集，而不会导致以磁盘为中心架构的开销

1. Joy Arulraj, Andrew Pavlo, and Subramanya R. Dulloor:
     “[Let's Talk About Storage & Recovery Methods for Non-Volatile Memory Database Systems](http://www.pdl.cmu.edu/PDL-FTP/NVM/storage.pdf),” at *ACM International Conference on
     Management of Data* (SIGMOD), June 2015.
     [doi:10.1145/2723372.2749441](http://dx.doi.org/10.1145/2723372.2749441)

     > 在内存中保存所有内容
     >
     > ……如果将来非易失性存储技术得到更广泛普及，可能还需要进一步改变存储引擎设计

1. Edgar F. Codd, S. B. Codd, and C. T. Salley:
     “[Providing OLAP to User-Analysts: An IT Mandate](https://pdfs.semanticscholar.org/a0bd/1491a54a4de428c5eef9b836ef6ee2915fe7.pdf),”
     E. F. Codd Associates, 1993.

     > 事务处理与分析处理
     >
     > ……为了区分使用数据库与事务处理的模式，称之为在线分析处理（online analytic processing，OLAP）

1. Surajit Chaudhuri and Umeshwar Dayal:
     “[An Overview of Data Warehousing and OLAP Technology](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/sigrecord.pdf),” *ACM SIGMOD Record*, volume 26, number 1, pages 65–74,
     March 1997. [doi:10.1145/248603.248616](http://dx.doi.org/10.1145/248603.248616)

     > 数据仓库
     >
     > ……数据仓库是单独的数据库，分析人员可以在不影响 OLTP 操作的情况下尽情地使用

1. Per-Åke Larson, Cipri Clinciu, Campbell Fraser, et al.:
     “[Enhancements to SQL Server Column Stores](http://research.microsoft.com/pubs/193599/Apollo3%20-%20Sigmod%202013%20-%20final.pdf),” at *ACM International Conference on Management of Data*
     (SIGMOD), June 2013.

1. Franz Färber, Norman May, Wolfgang Lehner, et al.:
     “[The SAP HANA Database – An Architecture Overview](http://sites.computer.org/debull/A12mar/hana.pdf),”
     *IEEE Data Engineering Bulletin*, volume 35, number 1, pages 28–33, March 2012.

1. Michael Stonebraker:
     “[The Traditional RDBMS Wisdom Is (Almost Certainly) All Wrong](http://slideshot.epfl.ch/talks/166),” presentation at *EPFL*, May 2013.

     > OLTP 数据库和数据仓库之间的差异
     >
     > ……然而，它们越来越分为两个独立的存储和查询引擎，这些引擎卡号可以通过一个通用的 SQL 界面进行访问

1. Daniel J. Abadi:
     “[Classifying the SQL-on-Hadoop Solutions](https://web.archive.org/web/20150622074951/http://hadapt.com/blog/2013/10/02/classifying-the-sql-on-hadoop-solutions/),” *hadapt.com*, October 2, 2013.

1. Marcel Kornacker, Alexander Behm, Victor Bittorf, et al.:
     “[Impala: A Modern, Open-Source SQL Engine for Hadoop](http://pandis.net/resources/cidr15impala.pdf),” at *7th Biennial Conference on Innovative Data Systems
     Research* (CIDR), January 2015.

     > OLTP 数据库和数据仓库之间的差异
     >
     > ……最近，还出现了大量开源的基于 Hadoop的 SQL 项目，包括 Apache Hive

1. Sergey Melnik, Andrey Gubarev, Jing Jing Long, et al.:
     “[Dremel: Interactive Analysis of Web-Scale Datasets](https://research.google/pubs/pub36632/),” at *36th International Conference on Very Large Data Bases* (VLDB), pages
     330–339, September 2010.

     > OLTP 数据库和数据仓库之间的差异
     >
     > ……其中一些系统是基于 Google Dremel 而构建的

1. Ralph Kimball and Margy Ross:
     *The Data Warehouse Toolkit: The Definitive Guide to Dimensional Modeling*,
     3rd edition. John Wiley & Sons, July 2013. ISBN: 978-1-118-53080-1

     > 星型与雪花型分析模式
     >
     > ……许多数据仓库都相当公式化的使用了星型模式，也称为维度建模

1. Derrick Harris:
     “[Why Apple, eBay, and Walmart Have Some of the Biggest Data Warehouses You’ve Ever Seen](http://gigaom.com/2013/03/27/why-apple-ebay-and-walmart-have-some-of-the-biggest-data-warehouses-youve-ever-seen/),”
     *gigaom.com*, March 27, 2013.

     > 星型与雪花型分析模式
     >
     > …… 像苹果、沃尔玛或者 ebay 这样的大企业，其数据仓库可能有数十PB的交易历史，其中大部分都保存在事实表中

1. Julien Le Dem:
     “[Dremel Made Simple with Parquet](https://blog.twitter.com/engineering/en_us/a/2013/dremel-made-simple-with-parquet.html),”
     *blog.twitter.com*, September 11, 2013.

     > 列式存储
     >
     > ……例如，Paruet 是基于 Google 的 Dremel 的一种支持文档数据模型的列存储格式

1. Daniel J. Abadi, Peter Boncz, Stavros
     Harizopoulos, et al.:
     “[The Design and Implementation of Modern Column-Oriented Database Systems](http://cs-www.cs.yale.edu/homes/dna/papers/abadi-column-stores.pdf),” *Foundations and Trends in
     Databases*, volume 5, number 3, pages 197–280, December 2013.
     [doi:10.1561/1900000024](http://dx.doi.org/10.1561/1900000024)

     > 列压缩
     >
     > ……对于不同类型的数据，还有各种其他压缩方法

1. Peter Boncz, Marcin Zukowski, and Niels Nes:
     “[MonetDB/X100: Hyper-Pipelining Query Execution](http://cidrdb.org/cidr2005/papers/P19.pdf),”
     at *2nd Biennial Conference on Innovative Data Systems Research* (CIDR), January 2005.

1. Jingren Zhou and Kenneth A. Ross:
     “[Implementing Database Operations Using SIMD Instructions](http://www1.cs.columbia.edu/~kar/pubsk/simd.pdf),”
     at *ACM International Conference on Management of Data* (SIGMOD), pages 145–156, June 2002.
     [doi:10.1145/564691.564709](http://dx.doi.org/10.1145/564691.564709)

     > 内存带宽和矢量化处理
     >
     > ……分析数据库的开发人员还要关系如何高效地将内存的带宽用于 CPU 缓存，避免分支错误预测和 CPU 指令处理流水线中的气泡，并利用现代 CPU 的单指令多数据（SIMD）指令[59，60] 

1. Michael Stonebraker, Daniel J. Abadi, Adam Batkin, et al.:
     “[C-Store: A Column-oriented DBMS](http://www.cs.umd.edu/~abadi/vldb.pdf),”
     at *31st International Conference on Very Large Data Bases* (VLDB), pages 553–564, September 2005.

1. Andrew Lamb, Matt Fuller, Ramakrishna Varadarajan, et al.:
     “[The Vertica Analytic Database: C-Store 7 Years Later](http://vldb.org/pvldb/vol5/p1790_andrewlamb_vldb2012.pdf),”
     *Proceedings of the VLDB Endowment*, volume 5, number 12, pages 1790–1801, August 2012.

     > 列存储中的排序
     >
     > ……C-Store 最早引入了一种改进想法，并被商业数据仓库 Vertica[61，62]所采用

1. Julien Le Dem and Nong Li:
     “[Efficient Data Storage for Analytics with Apache Parquet 2.0](http://www.slideshare.net/julienledem/th-210pledem),” at *Hadoop Summit*, San Jose,
     June 2014.

     > 聚合：数据立方体与物化视图
     >
     > ……然而，对于临时分析查询，列存储性能要快得多，因此它正在迅速普及

1. Jim Gray, Surajit Chaudhuri, Adam Bosworth, et al.:
     “[Data Cube: A Relational Aggregation Operator Generalizing Group-By, Cross-Tab, and Sub-Totals](http://arxiv.org/pdf/cs/0701155.pdf),” *Data Mining and Knowledge
     Discovery*, volume 1, number 1, pages 29–53, March 2007.
     [doi:10.1023/A:1009726021843](http://dx.doi.org/10.1023/A:1009726021843)

     > 聚合：数据立方体与物化视图
     >
     > ……物化视图常见的一种特殊情况称为数据立方体或 OLAP 立方体

