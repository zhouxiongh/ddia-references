Designing Data-Intensive Applications
=====================================

Chapter 6 Partitioning
--------------------

1. David J. DeWitt and Jim N. Gray:
    “[Parallel Database Systems: The Future of High Performance Database Systems](http://www.cs.cmu.edu/~pavlo/courses/fall2013/static/papers/dewittgray92.pdf),”
    *Communications of the ACM*, volume 35, number 6, pages 85–98, June 1992.
    [doi:10.1145/129888.129894](http://dx.doi.org/10.1145/129888.129894)

    > ……分区数据库最初在20世纪80年代由 Teradata 和 Tandem NonStop SQL 等率先推出，最近又被一些 NoSQL 数据厍和基于 hadoop 的数据仓库重视起来

1. Lars George:
    “[HBase vs. BigTable Comparison](http://www.larsgeorge.com/2009/11/hbase-vs-bigtable-comparison.html),”
    *larsgeorge.com*, November 2009.

1. “[The Apache HBase Reference Guide](https://hbase.apache.org/book/book.html),” Apache Software Foundation, *hbase.apache.org*, 2014.

1. MongoDB, Inc.:
    “[New Hash-Based Sharding Feature in MongoDB 2.4](https://www.mongodb.com/blog/post/new-hash-based-sharding-feature-in-mongodb-24),” *blog.mongodb.org*, April 10, 2013.

    > 基于关键字区间分区
    >
    > ……采用这种分区策略的系统包括 bigtable，bigtable 的开源版本 HBase[2，3]，RethinkDB 和 2.4 版本之前 MongoDB[4]

1. Ikai Lan:
    “[App Engine Datastore Tip: Monotonically Increasing Values Are Bad](http://ikaisays.com/2011/01/25/app-engine-datastore-tip-monotonically-increasing-values-are-bad/),” *ikaisays.com*,
    January 25, 2011.

    > 基于关键字区间分区
    >
    > ……当测量数据从传感器写入数据库时，所有的写入操作都集中在同一个分区。这会导致该分区在写入时负载过高，而其他分区始终处于空闲状态

1. Martin Kleppmann:
    “[Java's hashCode Is Not Safe for Distributed Systems](http://martin.kleppmann.com/2012/06/18/java-hashcode-unsafe-for-distributed-systems.html),” *martin.kleppmann.com*, June 18, 2012.

    > 基于关键字哈希值分区
    >
    > ……许多编程语言也有内置的简单哈希函数，但是注意这些内置的哈希函数可能不适合分区，例如，Java 的 object.hashcode 和 Ruby 的 Object#hash，同一个键在不同的进程中可能返回不同的哈希值

1. David Karger, Eric Lehman, Tom Leighton, et al.:
    “[Consistent Hashing and Random Trees: Distributed Caching Protocols for Relieving Hot Spots on the World Wide Web](http://www.akamai.com/dl/technical_publications/ConsistenHashingandRandomTreesDistributedCachingprotocolsforrelievingHotSpotsontheworldwideweb.pdf),”
    at *29th Annual ACM Symposium on Theory of Computing* (STOC), pages 654–663, 1997.
    [doi:10.1145/258533.258660](http://dx.doi.org/10.1145/258533.258660)

    > 一致性哈希
    >
    > 一致性哈希，由 Karger 等人首先提出，是一种评价分配负载的方法，最初用于 CDN 等互联网缓存系统

1. John Lamping and Eric Veach:
    “[A Fast, Minimal Memory, Consistent Hash Algorithm](http://arxiv.org/pdf/1406.2294v1.pdf),” *arxiv.org*, June 2014.

1. Eric Redmond:
    “[A Little Riak Book](https://web.archive.org/web/20160807123307/http://www.littleriakbook.com/),” Version 1.4.0,
    Basho Technologies, September 2013.

1. “[Couchbase 2.5 Administrator Guide](http://docs.couchbase.com/couchbase-manual-2.5/cb-admin/),” Couchbase, Inc., 2014.

    > 基于关键字的哈希值分区
    >
    > ……而Riak[9]、Couchbase[10] 和 Voldemort 干脆就不支持关键字上的区间查询

1. Avinash Lakshman and Prashant Malik:
      “[Cassandra – A Decentralized Structured Storage System](http://www.cs.cornell.edu/Projects/ladis2009/papers/Lakshman-ladis2009.PDF),” at *3rd ACM SIGOPS International Workshop on
      Large Scale Distributed Systems and Middleware* (LADIS), October 2009.

1. Jonathan Ellis:
      “[Facebook’s Cassandra Paper, Annotated and Compared to Apache Cassandra 2.0](https://docs.datastax.com/en/articles/cassandra/cassandrathenandnow.html),”
      *docs.datastax.com*, September 12, 2013.

1. “[Introduction to Cassandra Query Language](https://docs.datastax.com/en/cql-oss/3.1/cql/cql_intro_c.html),” DataStax, Inc., 2014.

      > 基于关键字的哈希值分区
      >
      > ……Cassandra 则在两种分区策略之间做了一个折中[11-13]

1. Samuel Axon:
      “[3% of Twitter's Servers Dedicated to Justin Bieber](http://mashable.com/2010/09/07/justin-bieber-twitter/),” *mashable.com*, September 7, 2010.

      > 负载倾斜与热点
      >
      > ……例如，在社交媒体上，一些名人用户有数百万的粉丝，当其发布一些热点事件时可能会引发一场访问风暴，出现大量对相同关键字的写操作（其中关键字可能是名人的用户 ID，或则人们正在评论的事件 ID）

1. “[Riak KV Docs](https://docs.riak.com/riak/kv/latest/index.html),” *docs.riak.com*.

1. Richard Low:
      “[The Sweet Spot for Cassandra Secondary Indexing](https://web.archive.org/web/20190831132955/http://www.wentnet.com/blog/?p=77),” *wentnet.com*, October 21, 2013.

1. Zachary Tong:
      “[Customizing Your Document Routing](https://www.elastic.co/blog/customizing-your-document-routing/),” *elastic.co*, June 3, 2013.

1. “[Apache Solr Reference Guide](https://cwiki.apache.org/confluence/display/solr/Apache+Solr+Reference+Guide),” Apache Software Foundation, 2014.

1. Andrew Pavlo:
      “[H-Store Frequently Asked Questions](http://hstore.cs.brown.edu/documentation/faq/),”
      *hstore.cs.brown.edu*, October 2013.

      > 基于文档分区的二级索引
      >
      > ……尽管如此，它还是广泛用于实践，MongoDB、Riak[15]、Cassandra[16]、Elasticsearch[17]、SolrCloud[18] 和 VoltDB[19] 都支持基于文档分区二级索引

1. “[Amazon DynamoDB Developer Guide](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/),” Amazon Web Services, Inc., 2014.

      > 基于词条的二级索引分区
      >
      > ……例如，Aoazon DynamoDB 的二级索引通常可以在1秒之内完成更新，但当底层设施出现故障时，也有可能需要等待很长的时间

1. Rusty Klophaus:
      “[Difference Between 2I and Search](https://web.archive.org/web/20150926053350/http://lists.basho.com/pipermail/riak-users_lists.basho.com/2011-October/006220.html),” email to *riak-users* mailing list, *lists.basho.com*, October 25, 2011.

1. Donald K. Burleson:
      “[Object Partitioning in Oracle](http://www.dba-oracle.com/art_partit.htm),”
      *dba-oracle.com*, November 8, 2000.

      > 基于词条的二级索引分区
      >
      > ……其他使用全局索引的系统还包括 Riak 的搜索功能和 Oracle 数据仓库，后者允许用户来选择是使用本地还是全局索引

1. Eric Evans:
      “[Rethinking Topology in Cassandra](http://www.slideshare.net/jericevans/virtual-nodes-rethinking-topology-in-cassandra),” at *ApacheCon Europe*, November 2012.

      > 动态分区
      >
      > ……如果只有少量的数据，少量的分区就足够了，这样系统开销很小；如果有大量的数据，每个分区的大小则被限制在一个可配的最大值

1. Rafał Kuć:
      “[Reroute API Explained](http://elasticsearchserverbook.com/reroute-api-explained/),”
      *elasticsearchserverbook.com*, September 30, 2013.

      > 动态再平衡的策略
      >
      > ……Riak、Elasticsearch、Couchbase 和 Voldemort 都支持这种动态平衡方法

1. “[Project Voldemort Documentation](http://www.project-voldemort.com/voldemort/),” *project-voldemort.com*.

1. Enis Soztutar:
      “[Apache HBase Region Splitting and Merging](http://hortonworks.com/blog/apache-hbase-region-splitting-and-merging/),” *hortonworks.com*, February 1, 2013.

      > 动态再平衡的策略
      >
      > ……对于关键字区间分区，预分裂要求已经知道一些关键字的分布情况

1. Brandon Williams:
      “[Virtual Nodes in Cassandra 1.2](http://www.datastax.com/dev/blog/virtual-nodes-in-cassandra-1-2),” *datastax.com*, December 4, 2012.

1. Richard Jones:
      “[libketama: Consistent Hashing Library for Memcached Clients](https://www.metabrew.com/article/libketama-consistent-hashing-algo-memcached-clients),” *metabrew.com*, April 10, 2007.

      > 按节点比例分区
      >
      > ……换句话说，每个节点具有固定数量的分区[23，27，28]

1. Branimir Lambov:
      “[New Token Allocation Algorithm in Cassandra 3.0](http://www.datastax.com/dev/blog/token-allocation-algorithm),” *datastax.com*, January 28, 2016.

      > 按节点比例分区
      >
      > Cassandra 在3.0 时推出了改进算法，可以避免上述不公平的分裂

1. Jason Wilder:
      “[Open-Source Service Discovery](http://jasonwilder.com/blog/2014/02/04/service-discovery-in-the-cloud/),” *jasonwilder.com*, February 2014.

      > 请求路由
      >
      > ……许多公司已经开发自己的内部服务发现工具，其中很多已经开源

1. Kishore Gopalakrishna, Shi Lu, Zhen Zhang, et al.:
      “[Untangling Cluster Management with Helix](http://www.socc2012.org/helix_onecol.pdf?attredirects=0),” at *ACM Symposium on Cloud Computing* (SoCC), October 2012.
      [doi:10.1145/2391229.2391248](http://dx.doi.org/10.1145/2391229.2391248)

      > 请求路由
      >
      > ……例如，LinkedIn 的 Espresso 使用 Helix 进行集群管理（底层是 ZooKeeper）

1. “[Moxi 1.8 Manual](http://docs.couchbase.com/moxi-manual-1.8/),” Couchbase, Inc., 2014.

      > 请求路由
      >
      > ……它通过配置一个名为 moxi 的路由选择层，向集群节点学习最新的路由变化

1. Shivnath Babu and Herodotos Herodotou:
      “[Massively Parallel Databases and MapReduce Systems](https://www.microsoft.com/en-us/research/wp-content/uploads/2013/11/db-mr-survey-final.pdf),”
      *Foundations and Trends in Databases*, volume 5, number 1, pages 1–104, November 2013.
      [doi:10.1561/1900000036](http://dx.doi.org/10.1561/1900000036)

      > 并行查询执行
      >
      > ……有关并行数据库更多相关技术细节请参考文献

