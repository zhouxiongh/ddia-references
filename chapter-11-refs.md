Designing Data-Intensive Applications
=====================================

Chapter 11 Stream Processing
--------------------

1. Tyler Akidau, Robert Bradshaw, Craig Chambers, et al.:
    “[The Dataflow Model: A Practical Approach to Balancing Correctness, Latency, and Cost in Massive-Scale, Unbounded, Out-of-Order Data Processing](http://www.vldb.org/pvldb/vol8/p1792-Akidau.pdf),”
    *Proceedings of the VLDB Endowment*, volume 8, number 12, pages 1792–1803, August 2015.
    [doi:10.14778/2824032.2824076](http://dx.doi.org/10.14778/2824032.2824076)

    > 除非业务停止，否则这个过程永远不会结束，因此数据集永远不会以任何有意义的方式“完成”

1. Harold Abelson, Gerald Jay Sussman, and Julie Sussman:
    [*Structure and Interpretation of Computer Programs*](https://mitpress.mit.edu/sicp/),
    2nd edition. MIT Press, 1996. ISBN: 978-0-262-51087-5, available online at *mitpress.mit.edu*

    > 一般来说，“流”是指随着时间的推移而持续可用的数据。编程语言（lazy lists）[2]

1. Patrick Th. Eugster, Pascal A. Felber,
    Rachid Guerraoui, and Anne-Marie Kermarrec:
    “[The Many Faces of Publish/Subscribe](http://www.cs.ru.nl/~pieter/oss/manyfaces.pdf),”
    *ACM Computing Surveys*, volume 35, number 2, pages 114–131, June 2003.
    [doi:10.1145/857076.857078](http://dx.doi.org/10.1145/857076.857078)

    > 发送事件流
    >
    > ……在流术语中，事件由生产者生成一次，然后可能由多个消费者[3]处理

1. Joseph M. Hellerstein and Michael Stonebraker:
    [*Readings in Database Systems*](http://redbook.cs.berkeley.edu/), 4th edition.
    MIT Press, 2005. ISBN: 978-0-262-69314-1, available online at *redbook.cs.berkeley.edu*

1. Don Carney, Uğur Çetintemel, Mitch Cherniack, et al.:
    “[Monitoring Streams – A New Class of Data Management Applications](http://www.vldb.org/conf/2002/S07P02.pdf),” at *28th International Conference on Very Large Data Bases*
    (VLDB), August 2002.

    > 发送时间流
    >
    > ……但是他们（数据库）的功能非常有限，在数据库设计中有点事后考虑的意思[4，5]

1. Matthew Sackman:
    “[Pushing Back](http://www.lshift.net/blog/2016/05/05/pushing-back/),”
    *lshift.net*, May 5, 2016.

    > 消息系统
    >
    > ……如果消息是在队列中缓冲的，那么了解队列增长时的情况是很重要的。如果队列不再适合在内存中，系统是否会崩溃，或者是否会将消息写入磁盘？如果是这样，磁盘访问是如何影响消息系统的性能的[6]？

1. Vicent Martí:
    “[Brubeck, a statsd-Compatible Metrics Aggregator](http://githubengineering.com/brubeck/),” *githubengineering.com*, June 15, 2015.

    > 消息丢失是否可以接受，在很大程度上取决于应用。例如，对于定期传输的传感器读数和指标，偶尔丢失的数据点也许并不重要，因为无论如何，更新的值会在短时间内被发送。然而，要注意的是，如果有大量的消息被丢弃，可能不会立即看出指标不正确[7]。如果你在计算事件，更重要的是它们被可靠地传递，因为每个丢失的消息都意味着不正确的计数器。

1. Seth Lowenberger:
      “[MoldUDP64   Protocol Specification V 1.00](http://www.nasdaqtrader.com/content/technicalsupport/specifications/dataproducts/moldudp64.pdf),” *nasdaqtrader.com*, July 2009.

      >  UDP组播被广泛用于金融行业的流媒体，如股票市场反馈，其中低延迟是很重要的[8]。虽然UDP本身是不可靠的，但应用级协议可以恢复丢失的数据包（生产者必须记住它已经发送的数据包，以便它可以根据需要重新传输）。

1. Pieter Hintjens:
      [*ZeroMQ – The Guide*](http://zguide.zeromq.org/page:all). O'Reilly Media, 2013.
      ISBN: 978-1-449-33404-8

      >  ZeroMQ[9]和nanomsg等无经纪人消息库采取了类似的方法，通过TCP或IP组播实现发布/订阅消息。

1. Ian Malpass:
      “[Measure   Anything, Measure Everything](https://codeascraft.com/2011/02/15/measure-anything-measure-everything/),” *codeascraft.com*, February 15, 2011.

1. Dieter Plaetinck:
      “[25 Graphite, Grafana and statsd Gotchas](https://grafana.com/blog/2016/03/03/25-graphite-grafana-and-statsd-gotchas/),”
      *grafana.com*, March 3, 2016.

      >  StatsD[10]和Brubeck[7]使用不可靠的UDP消息传递来收集网络上所有机器的度量并对其进行监控。(在StatsD协议中，只有当所有的消息都被收到时，计数器的指标才是正确的；使用UDP最多只能使指标变得近似[11]。参见 "TCP与UDP"）。

1. Jeff Lindsay:
      “[Web Hooks to Revolutionize the Web](http://progrium.com/blog/2007/05/03/web-hooks-to-revolutionize-the-web/),” *progrium.com*, May 3, 2007.

      > 如果消费者在网络上公开了一个服务，生产者可以直接提出HTTP或RPC请求（见 "通过服务的数据流：REST和RPC"），将消息推送给消费者。这就是webhooks[12]背后的想法，一种模式是一个服务的回调URL被注册到另一个服务中，每当事件发生时，它就向该URL发出请求。

1. Jim N. Gray:
      “[Queues Are Databases](https://arxiv.org/pdf/cs/0701158.pdf),”
      Microsoft Research Technical Report MSR-TR-95-56, December 1995.

      > 一个广泛使用的替代方法是通过消息代理（也被称为消息队列）发送消息，它本质上是一种为处理消息流而优化的数据库[13]。它作为一个服务器运行，生产者和消费者作为客户连接到它。生产者向经纪人写消息，而消费者通过从经纪人那里读取消息来接收消息。

1. Mark Hapner, Rich Burridge, Rahul Sharma, et al.:
      “[JSR-343 Java Message Service (JMS) 2.0 Specification](https://jcp.org/en/jsr/detail?id=343),” *jms-spec.java.net*, March 2013.

1. Sanjay Aiyagari, Matthew Arrott, Mark Atwell, et al.:
      “[AMQP: Advanced Message Queuing Protocol Specification](http://www.rabbitmq.com/resources/specs/amqp0-9-1.pdf),” Version 0-9-1, November 2008.

1. “[Google Cloud Pub/Sub: A Google-Scale Messaging Service](https://cloud.google.com/pubsub/architecture),” *cloud.google.com*, 2016.

      > 这是消息代理的传统观点，它被封装在JMS[14]和AMQP[15]等标准中，并在RabbitMQ、ActiveMQ、HornetQ、Qpid、TIBCO Enterprise Message Service、IBM MQ、Azure Service Bus和Google Cloud Pub/Sub[16]等软件中实现。

1. “[Apache Kafka 0.9 Documentation](http://kafka.apache.org/documentation.html),” *kafka.apache.org*, November 2015.

1. Jay Kreps, Neha Narkhede, and Jun Rao:
      “[Kafka: A Distributed Messaging System for Log Processing](https://www.microsoft.com/en-us/research/wp-content/uploads/2017/09/Kafka.pdf),” at *6th International Workshop on
      Networking Meets Databases* (NetDB), June 2011.

1. “[Amazon Kinesis Streams Developer Guide](http://docs.aws.amazon.com/streams/latest/dev/introduction.html),” *docs.aws.amazon.com*, April 2016.

1. Leigh Stewart and Sijie Guo:
      “[Building DistributedLog: Twitter’s High-Performance Replicated Log Service](https://blog.twitter.com/2015/building-distributedlog-twitter-s-high-performance-replicated-log-service),” *blog.twitter.com*,
      September 16, 2015.

1. “[DistributedLog Documentation](https://bookkeeper.apache.org/distributedlog/docs/latest/),”
      Apache Software Foundation, *distributedlog.io*.

1. Jay Kreps:
      “[Benchmarking Apache Kafka: 2 Million Writes Per Second (On Three Cheap Machines)](https://engineering.linkedin.com/kafka/benchmarking-apache-kafka-2-million-writes-second-three-cheap-machines),” *engineering.linkedin.com*,
      April 27, 2014.

1. Kartik Paramasivam:
      “[How We’re Improving and Advancing Kafka at LinkedIn](https://engineering.linkedin.com/apache-kafka/how-we_re-improving-and-advancing-kafka-linkedin),” *engineering.linkedin.com*, September 2, 2015.

      > Apache Kafka[17, 18]、Amazon Kinesis Streams[19]和Twitter的DistributedLog[20, 21]都是基于日志的消息中介，其工作方式与此类似。谷歌云Pub/Sub在架构上类似，但暴露了一个JMS风格的API，而不是一个日志抽象[16]。尽管这些消息中介把所有的消息都写到了磁盘上，但通过在多台机器上进行分区，它们能够实现每秒数百万条消息的吞吐量，并通过复制消息实现容错[22, 23]。

1. Jay Kreps:
      “[The Log: What Every Software Engineer Should Know About Real-Time Data's Unifying Abstraction](http://engineering.linkedin.com/distributed-systems/log-what-every-software-engineer-should-know-about-real-time-datas-unifying),”
      *engineering.linkedin.com*, December 16, 2013.

      > 这方面使得基于日志的消息传递更像上一章的批处理过程，通过可重复的转换过程，将衍生数据与输入数据明确分开。它允许更多的实验，更容易从错误和bug中恢复，使其成为组织内整合数据流的好工具[24]。

1. Shirshanka Das, Chavdar Botev, Kapil Surlaker,
      et al.: “[All Aboard the Databus!](http://www.socc2012.org/s18-das.pdf),” at *3rd ACM
      Symposium on Cloud Computing* (SoCC), October 2012.

1. Yogeshwer Sharma, Philippe Ajoux, Petchean Ang, et al.:
      “[Wormhole: Reliable Pub-Sub to Support Geo-Replicated Internet Services](https://www.usenix.org/system/files/conference/nsdi15/nsdi15-paper-sharma.pdf),” at *12th USENIX Symposium on
      Networked Systems Design and Implementation* (NSDI), May 2015.

1. P. P. S. Narayan:
      “[Sherpa Update](http://web.archive.org/web/20160801221400/https://developer.yahoo.com/blogs/ydn/sherpa-7992.html),”
      *developer.yahoo.com*, June 8, .

1. Martin Kleppmann:
      “[Bottled Water: Real-Time Integration of PostgreSQL and Kafka](http://martin.kleppmann.com/2015/04/23/bottled-water-real-time-postgresql-kafka.html),” *martin.kleppmann.com*, April 23, 2015.

1. Ben Osheroff:
      “[Introducing Maxwell, a mysql-to-kafka Binlog Processor](https://web.archive.org/web/20170208100334/https://developer.zendesk.com/blog/introducing-maxwell-a-mysql-to-kafka-binlog-processor),”
      *developer.zendesk.com*, August 20, 2015.

1. Randall Hauch:
      “[Debezium 0.2.1 Released](http://debezium.io/blog/2016/06/10/Debezium-0/),” *debezium.io*,
      June 10, 2016.

1. Prem Santosh Udaya Shankar:
      “[Streaming MySQL Tables in Real-Time to Kafka](https://engineeringblog.yelp.com/2016/08/streaming-mysql-tables-in-real-time-to-kafka.html),” *engineeringblog.yelp.com*, August 1, 2016.

1. “[Mongoriver](https://github.com/stripe/mongoriver),”
      Stripe, Inc., *github.com*, September 2014.

1. Dan Harvey:
      “[Change Data Capture with Mongo + Kafka](http://www.slideshare.net/danharvey/change-data-capture-with-mongodb-and-kafka),” at *Hadoop Users Group UK*, August 2015.

1. “[Oracle GoldenGate 12c: Real-Time Access to Real-Time Information](http://www.oracle.com/us/products/middleware/data-integration/oracle-goldengate-realtime-access-2031152.pdf),” Oracle White Paper, March 2015.

1. “[Oracle GoldenGate Fundamentals: How Oracle GoldenGate Works](https://www.youtube.com/watch?v=6H9NibIiPQE),” Oracle Corporation, *youtube.com*, November 2012.

      > LinkedIn的Databus[25]，Facebook的Wormhole[26]，以及雅虎的Sherpa[27]都大规模地使用了这个想法。Bottled Water使用解码写头日志的API为PostgreSQL实现了CDC[28]，Maxwell和Debezium通过解析binlog为MySQL做了类似的工作[29, 30, 31]，Mongoriver读取MongoDB的oplog[32, 33]，GoldenGate为Oracle提供了类似的设施[34, 35]。

1. Slava Akhmechet:
      “[Advancing the Realtime Web](http://rethinkdb.com/blog/realtime-web/),” *rethinkdb.com*,
      January 27, 2015.

1. “[Firebase Realtime Database Documentation](https://firebase.google.com/docs/database/),” Google, Inc., *firebase.google.com*, May 2016.

1. “[Apache CouchDB 1.6 Documentation](http://docs.couchdb.org/en/latest/),” *docs.couchdb.org*, 2014.

1. Matt DeBergalis:
      “[Meteor 0.7.0: Scalable Database Queries Using MongoDB Oplog Instead of Poll-and-Diff](http://info.meteor.com/blog/meteor-070-scalable-database-queries-using-mongodb-oplog-instead-of-poll-and-diff),” *info.meteor.com*,
      December 17, 2013.

      > 越来越多的数据库开始支持变化流作为第一类接口，而不是典型的改装和反向工程的CDC工作。例如，RethinkDB允许查询在查询结果发生变化时订阅通知[36]，Firebase[37]和CouchDB[38]提供基于变化源的数据同步，该变化源也提供给应用程序，Meteor使用MongoDB oplog来订阅数据变化并更新用户界面[39]。

1. “[Chapter 15. Importing and Exporting Live Data](https://docs.voltdb.com/UsingVoltDB/ChapExport.php),” VoltDB 6.4 User Manual, *docs.voltdb.com*, June 2016.

      > VoltDB允许事务以流的形式从数据库持续输出数据[40]。数据库将关系数据模型中的输出流表示为一个表，事务可以向其中插入图元，但不能查询。然后，流由已提交的事务写到这个特殊的表的图元日志组成，按照它们被提交的顺序。外部消费者可以异步地消费这个日志，并使用它来更新派生数据系统。

1. Neha Narkhede:
      “[Announcing Kafka Connect: Building Large-Scale Low-Latency Data Pipelines](http://www.confluent.io/blog/announcing-kafka-connect-building-large-scale-low-latency-data-pipelines),” *confluent.io*,
      February 18, 2016.

      > Kafka Connect[41]是一项将广泛的数据库系统的变化数据采集工具与Kafka集成的努力。一旦变更事件流进入Kafka，它就可以被用来更新衍生的数据系统，如搜索索引，也可以进入本章后面讨论的流处理系统。

1. Greg Young:
      “[CQRS and Event Sourcing](https://www.youtube.com/watch?v=JHGkaShoyNs),” at *Code on
      the Beach*, August 2014.

1. Martin Fowler:
      “[Event Sourcing](http://martinfowler.com/eaaDev/EventSourcing.html),” *martinfowler.com*,
      December 12, 2005.

1. Vaughn Vernon:
      [*Implementing Domain-Driven Design*](https://www.informit.com/store/implementing-domain-driven-design-9780321834577).
      Addison-Wesley Professional, 2013. ISBN: 978-0-321-83457-7

      > 我们在这里讨论的想法和事件源之间有一些相似之处，事件源是在领域驱动设计（DDD）社区开发的一种技术[42, 43, 44]。我们将简单地讨论事件源，因为它包含了一些对流式系统有用的相关想法。

1. H. V. Jagadish, Inderpal Singh Mumick, and Abraham Silberschatz:
      “[View Maintenance Issues for the Chronicle Data Model](https://dl.acm.org/doi/10.1145/212433.220201),”
      at *14th ACM SIGACT-SIGMOD-SIGART Symposium on Principles of Database Systems* (PODS), May 1995.
      [doi:10.1145/212433.220201](http://dx.doi.org/10.1145/212433.220201)

      > 事件源与编年史数据模型[45]相似，事件日志与你在星型模式中发现的事实表也有相似之处（见 "星星和雪花：分析的模式"）。

1. “[Event Store 3.5.0 Documentation](http://docs.geteventstore.com/),” Event Store LLP, *docs.geteventstore.com*, February 2016.

      > 专门的数据库，如Event Store[46]已经被开发出来，以支持使用事件源的应用，但一般来说，该方法与任何特定的工具无关。传统的数据库或基于日志的消息代理也可以用来建立这种风格的应用。

1. Martin Kleppmann:
      [*Making Sense of Stream Processing*](http://www.oreilly.com/data/free/stream-processing.csp). Report, O'Reilly Media, May 2016.

      > 因此，使用事件源的应用程序需要将事件日志（代表写入系统的数据），转化为适合展示给用户的应用状态（从系统中读取数据的方式[47]）。这种转换可以使用任意的逻辑，但它应该是确定性的，这样你就可以再次运行它并从事件日志中得出相同的应用状态。

1. Sander Mak:
      “[Event-Sourced Architectures with Akka](http://www.slideshare.net/SanderMak/eventsourced-architectures-with-akka),” at *JavaOne*, September 2014.

      > 事件源理念注意区分事件和命令[48]。当一个来自用户的请求第一次到达时，它最初是一个命令：此时它仍然可能失败，例如因为违反了一些完整性条件。应用程序必须首先验证它是否可以执行该命令。如果验证成功，命令被接受，它就成为一个事件，它是持久的和不可改变的。

1. Julian Hyde:
      [personal communication](https://twitter.com/julianhyde/status/743374145006641153),
      June 2016.

1. Ashish Gupta and Inderpal Singh Mumick:
      *Materialized Views: Techniques, Implementations, and Applications*. MIT Press, 1999.
      ISBN: 978-0-262-57122-7

1. Timothy Griffin and Leonid Libkin:
      “[Incremental Maintenance of Views with Duplicates](http://homepages.inf.ed.ac.uk/libkin/papers/sigmod95.pdf),” at *ACM International Conference on Management of
      Data* (SIGMOD), May 1995.
      [doi:10.1145/223784.223849](http://dx.doi.org/10.1145/223784.223849)

      > 如果你有数学上的倾向，你可以说应用状态是你在时间上整合事件流时得到的东西，而变化流是你通过时间区分状态时得到的东西，如图11-6所示[49, 50, 51]。这个类比有局限性（例如，状态的二阶导数似乎没有意义），但它是思考数据的一个有用的出发点。

1. Pat Helland:
      “[Immutability Changes Everything](http://cidrdb.org/cidr2015/Papers/CIDR15_Paper16.pdf),”
      at *7th Biennial Conference on Innovative Data Systems Research* (CIDR), January 2015.

      > 如果你持久地存储变化日志，这只是起到了使状态可重复的作用。如果你认为事件日志是你的记录系统，而任何可变的状态都是由它派生出来的，那么推理通过系统的数据流就变得容易了。正如Pat Helland所说[52]。

1. Martin Kleppmann:
      “[Accounting for Computer Scientists](http://martin.kleppmann.com/2011/03/07/accounting-for-computer-scientists.html),” *martin.kleppmann.com*, March 7, 2011.

      > 数据库中的不可变性是一个古老的想法。例如，会计人员在财务记账中使用不变性已经有几个世纪了。当交易发生时，它被记录在一个仅有的分类账中，该分类账本质上是一个描述金钱、货物或服务易手的事件日志。账目，如损益表或资产负债表，是通过将账簿中的交易相加得出的[53]。

1. Pat Helland:
      “[Accountants Don't Use Erasers](https://blogs.msdn.microsoft.com/pathelland/2007/06/14/accountants-dont-use-erasers/),” *blogs.msdn.com*, June 14, 2007.

      > 如果犯了错误，会计师不会删除或改变分类账中的错误交易--相反，他们会添加另一项交易来弥补错误，例如，退还错误的费用。错误的交易仍然永远保留在分类账中，因为它可能对审计工作很重要。如果从错误的分类账中得出的不正确的数字已经公布，那么下一个会计期间的数字就包括更正。这个过程在会计中是完全正常的[54]。

1. Fangjin Yang:
      “[Dogfooding with Druid, Samza, and Kafka: Metametrics at Metamarkets](https://metamarkets.com/2015/dogfooding-with-druid-samza-and-kafka-metametrics-at-metamarkets/),” *metamarkets.com*, June 3, 2015.

1. Gavin Li, Jianqiu Lv, and Hang Qi:
      “[Pistachio: Co-Locate the Data and Compute for Fastest Cloud Compute](https://web.archive.org/web/20181214032620/https://yahoohadoop.tumblr.com/post/116365275781/pistachio-co-locate-the-data-and-compute-for),”
      *yahoohadoop.tumblr.com*, April 13, 2015.

      > 此外，通过将易变的状态从不可变的事件日志中分离出来，你可以从同一个事件日志中衍生出几个不同的面向读的表示。这就像一个流有多个消费者一样（图11-5）：例如，分析数据库Druid使用这种方法直接从Kafka摄取数据[55]，Pistachio是一个分布式键值存储，使用Kafka作为提交日志[56]，而Kafka Connect汇可以从Kafka导出数据到各种不同的数据库和索引[41]。许多其他的存储和索引系统，如搜索服务器，同样从分布式日志中获取输入信息也是有意义的（见 "保持系统同步"）。

1. Kartik Paramasivam:
      “[Stream Processing Hard Problems – Part 1: Killing Lambda](https://engineering.linkedin.com/blog/2016/06/stream-processing-hard-problems-part-1-killing-lambda),” *engineering.linkedin.com*, June 27, 2016.

      > 有一个明确的从事件日志到数据库的转换步骤，使你的应用程序更容易随着时间的推移而发展：如果你想引入一个新的功能，以某种新的方式展示你现有的数据，你可以使用事件日志为新功能建立一个单独的阅读优化的视图，并与现有的系统一起运行，而无需修改它们。并排运行新旧系统往往比在现有系统中进行复杂的模式迁移要容易。一旦不再需要旧系统，你可以简单地关闭它并回收其资源[47, 57]。

1. Martin Fowler:
      “[CQRS](http://martinfowler.com/bliki/CQRS.html),” *martinfowler.com*, July 14, 2011.

1. Greg Young:
      “[CQRS Documents](https://cqrs.files.wordpress.com/2010/11/cqrs_documents.pdf),”
      *cqrs.files.wordpress.com*, November 2010.

      > 如果你不必担心数据如何被查询和访问，那么存储数据通常是很简单的；模式设计、索引和存储引擎的许多复杂性都是希望支持某些查询和访问模式的结果（见第3章）。由于这个原因，通过将数据的写入形式和读取形式分开，以及允许几种不同的读取视图，你可以获得很大的灵活性。这个想法有时被称为命令查询责任隔离（CQRS）[42, 58, 59]。

1. Baron Schwartz:
      “[Immutability, MVCC, and Garbage Collection](http://www.xaprb.com/blog/2013/12/28/immutability-mvcc-and-garbage-collection/),” *xaprb.com*, December 28, 2013.

1. Daniel Eloff, Slava Akhmechet, Jay Kreps, et al.:
      ["Re: Turning the Database Inside-out with Apache Samza](https://news.ycombinator.com/item?id=9145197)," Hacker News discussion, *news.ycombinator.com*, March 4, 2015.

      > 在多大程度上可以永远保持所有变化的不可改变的历史？答案取决于数据集的变化量。有些工作负载主要是添加数据，很少更新或删除；它们很容易成为不可更改的。其他工作负载在相对较小的数据集上有很高的更新和删除率；在这些情况下，不可更改的历史可能会增长得过大，碎片化可能成为一个问题，压缩和垃圾收集的性能对操作的稳健性变得至关重要[60, 61]。

1. “[Datomic Development Resources: Excision](http://docs.datomic.com/excision.html),” Cognitect, Inc., *docs.datomic.com*.

1. “[Fossil Documentation: Deleting Content from Fossil](http://fossil-scm.org/index.html/doc/trunk/www/shunning.wiki),” *fossil-scm.org*, 2016.

      > 在这些情况下，仅仅在日志中添加另一个事件来表明之前的数据应该被视为删除是不够的--你实际上想改写历史，假装这些数据一开始就没有被写入。例如，Datomic称这种功能为切除[62]，Fossil版本控制系统也有一个类似的概念，叫做避让[63]。

1. Jay Kreps:
      “[The irony of distributed systems is that data loss is really easy but deleting data is surprisingly hard,](https://twitter.com/jaykreps/status/582580836425330688)” *twitter.com*, March 30,
      2015.

      > 真正的删除数据是出乎意料的困难[64]，因为副本可以存在于许多地方：例如，存储引擎、文件系统和固态硬盘通常会写到一个新的位置，而不是原地覆盖[52]，而且备份通常是故意不可改变的，以防止意外删除或损坏。删除更多的是 "使数据更难检索 "的问题，而不是实际上 "使数据无法检索"。然而，你有时必须尝试，正如我们将在 "立法和自律 "中看到的。

1. David C. Luckham:
      “[What’s the Difference Between ESP and CEP?](http://www.complexevents.com/2006/08/01/what%E2%80%99s-the-difference-between-esp-and-cep/),” *complexevents.com*, August 1, 2006.

1. Srinath Perera:
      “[How Is Stream Processing and Complex Event Processing (CEP) Different?](https://www.quora.com/How-is-stream-processing-and-complex-event-processing-CEP-different),” *quora.com*, December 3, 2015.

      > 复杂事件处理（CEP）是20世纪90年代开发的一种分析事件流的方法，特别是针对那种需要搜索某些事件模式的应用[65, 66]。与正则表达式允许你搜索字符串中的某些字符模式的方式类似，CEP允许你指定规则来搜索流中的某些事件模式。

1. Arvind Arasu, Shivnath Babu, and Jennifer Widom:
      “[The CQL Continuous Query Language: Semantic Foundations and Query Execution](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/cql.pdf),”
      *The VLDB Journal*, volume 15, number 2, pages 121–142, June 2006.
      [doi:10.1007/s00778-004-0147-z](http://dx.doi.org/10.1007/s00778-004-0147-z)

      > CEP系统通常使用高水平的声明性查询语言，如SQL，或图形用户界面，来描述应该被检测的事件模式。这些查询被提交给一个处理引擎，该引擎消耗输入流并在内部维护一个执行所需匹配的状态机。当找到一个匹配时，引擎会发出一个复杂的事件（因此而得名），其中包括检测到的事件模式的细节[67]。

1. Julian Hyde:
      “[Data in Flight: How Streaming SQL Technology Can Help Solve the Web 2.0 Data Crunch](http://queue.acm.org/detail.cfm?id=1667562),” *ACM Queue*, volume 7, number 11, December 2009.
      [doi:10.1145/1661785.1667562](http://dx.doi.org/10.1145/1661785.1667562)

      > 在这些系统中，与普通数据库相比，查询和数据之间的关系是相反的。通常情况下，数据库持久地存储数据，并将查询视为短暂的：当一个查询进来时，数据库会搜索与查询相匹配的数据，然后在查询结束后将其遗忘。CEP引擎颠覆了这些角色：查询被长期存储，来自输入流的事件不断流过它们，以寻找与事件模式匹配的查询[68]。

1. “[Esper Reference, Version 5.4.0](http://esper.espertech.com/release-5.4.0/esper-reference/html_single/index.html),”
      EsperTech, Inc., *espertech.com*, April 2016.

1. Zubair Nabi, Eric Bouillet, Andrew Bainbridge, and Chris Thomas:
      “[Of Streams and Storms](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2014/04/Streams-and-Storm-April-2014-Final.pdf),” IBM technical report, *developer.ibm.com*, April 2014.

1. Milinda Pathirage, Julian Hyde, Yi Pan, and Beth Plale:
      “[SamzaSQL: Scalable Fast Data Management with Streaming SQL](https://github.com/milinda/samzasql-hpbdc2016/blob/master/samzasql-hpbdc2016.pdf),” at *IEEE International Workshop on
      High-Performance Big Data Computing* (HPBDC), May 2016.
      [doi:10.1109/IPDPSW.2016.141](http://dx.doi.org/10.1109/IPDPSW.2016.141)

      > CEP的实现包括Esper[69]、IBM InfoSphere Streams[70]、Apama、TIBCO StreamBase和SQLstream。像Samza这样的分布式流处理器也正在获得对流的声明性查询的SQL支持[71]。

1. Philippe Flajolet, Éric Fusy, Olivier
      Gandouet, and Frédéric Meunier:
      “[HyperLogLog: The Analysis of a Near-Optimal Cardinality Estimation Algorithm](http://algo.inria.fr/flajolet/Publications/FlFuGaMe07.pdf),”
      at *Conference on Analysis of Algorithms* (AofA), June 2007.

1. Jay Kreps:
      “[Questioning the Lambda Architecture](https://www.oreilly.com/ideas/questioning-the-lambda-architecture),” *oreilly.com*, July 2, 2014.

      > 流分析系统有时会使用概率算法，例如用于集合成员的布隆过滤器（我们在 "性能优化 "中遇到过），用于心数估计的HyperLogLog[72]，以及各种百分数估计算法（见 "实践中的百分数"）。概率算法产生近似的结果，但其优点是在流处理器中需要的内存比精确算法少得多。这种近似算法的使用有时会使人们认为流处理系统总是有损的、不精确的，但这是错误的：流处理本身并没有什么近似性，而概率算法只是一种优化[73]。

1. Ian Hellström:
      “[An Overview of Apache Streaming Technologies](https://databaseline.bitbucket.io/an-overview-of-apache-streaming-technologies/),” *databaseline.bitbucket.io*, March 12, 2016.

      > 许多开源的分布式流处理框架在设计时都考虑到了分析问题：例如，Apache Storm、Spark Streaming、Flink、Concord、Samza和Kafka Streams[74]。托管服务包括Google Cloud Dataflow和Azure Stream Analytics。

1. Jay Kreps:
      “[Why Local State Is a Fundamental Primitive in Stream Processing](https://www.oreilly.com/ideas/why-local-state-is-a-fundamental-primitive-in-stream-processing),” *oreilly.com*, July 31, 2014.

      > 原则上，任何流处理器都可以用于物化视图的维护，尽管需要永远维护事件与一些面向分析的框架的假设背道而驰，这些框架大多在有限的时间内操作窗口。Samza和Kafka Streams支持这种用法，建立在Kafka对日志压缩的支持之上[75]。

1. Shay Banon:
      “[Percolator](https://www.elastic.co/blog/percolator),” *elastic.co*, February 8,
      2011.

      > 例如，媒体监测服务订阅来自媒体机构的新闻文章和广播的馈送，并搜索任何提到公司、产品或感兴趣的话题的新闻。这是通过事先制定一个搜索查询，然后不断地将新闻项目流与该查询相匹配来完成的。一些网站也有类似的功能：例如，房地产网站的用户可以要求在市场上出现符合其搜索条件的新房产时得到通知。Elasticsearch的percolator功能[76]是实现这种流搜索的一个选择。

1. Alan Woodward and Martin Kleppmann:
      “[Real-Time Full-Text Search with Luwak and Samza](http://martin.kleppmann.com/2015/04/13/real-time-full-text-search-luwak-samza.html),” *martin.kleppmann.com*, April 13, 2015.

      > 传统的搜索引擎首先对文档进行索引，然后在索引上运行查询。与此相反，搜索流将处理过程转过来：查询被存储起来，而文档在查询后运行，就像在CEP中一样。在最简单的情况下，你可以针对每个查询测试每个文档，尽管如果你有大量的查询，这可能会变得很慢。为了优化这个过程，有可能对查询和文档进行索引，从而缩小可能匹配的查询集合[77]。

1. “[Apache Storm 2.1.0 Documentation](https://storm.apache.org/releases/2.1.0/index.html),” *storm.apache.org*, October 2019.

1. Tyler Akidau:
      “[The World Beyond Batch: Streaming 102](https://www.oreilly.com/ideas/the-world-beyond-batch-streaming-102),” *oreilly.com*, January 20, 2016.

      > 另一方面，许多流处理框架使用处理机器上的本地系统时钟（处理时间）来确定窗口化[79]。这种方法的优点是简单，如果事件创建和事件处理之间的延迟短得可以忽略不计，这种方法是合理的。然而，如果有任何明显的处理滞后，即如果处理可能明显晚于事件实际发生的时间，这种方法就失效了。

1. Stephan Ewen:
      “[Streaming Analytics with Apache Flink](https://www.confluent.io/resources/kafka-summit-2016/advanced-streaming-analytics-apache-flink-apache-kafka/),”
      at *Kafka Summit*, April 2016.

      > 如果有一个类比的话，可以考虑一下《星球大战》的电影：第四集于1977年上映，第五集于1980年上映，第六集于1983年上映，随后第一、二、三集分别于1999年、2002年和2005年上映，第七集于2015年上映[80]。ii如果你按照电影上映的顺序观看，你处理电影的顺序与它们叙述的顺序不一致。(集数就像事件的时间戳，而你观看电影的日期就是处理时间)。作为人类，我们能够应对这种不连续性，但流处理算法需要专门编写以适应这种时间和顺序问题。

1. Tyler Akidau, Alex Balikov, Kaya Bekiroğlu, et al.:
      “[MillWheel: Fault-Tolerant Stream Processing at Internet Scale](http://research.google.com/pubs/pub41378.html),” at *39th International Conference on Very Large Data Bases* (VLDB),
      August 2013.

      > 在某些情况下，有可能使用一个特殊的消息来表明，"从现在开始，不会再有时间戳早于t的消息"，这可以被消费者用来触发窗口[81]。然而，如果不同机器上的几个生产者正在产生事件，每个生产者都有自己的最小时间戳阈值，消费者需要单独跟踪每个生产者。在这种情况下，添加和删除生产者就比较麻烦。

1. Alex Dean:
      “[Improving Snowplow's Understanding of Time](http://snowplowanalytics.com/blog/2015/09/15/improving-snowplows-understanding-of-time/),” *snowplowanalytics.com*, September 15, 2015.

      > 为了调整不正确的设备时钟，一种方法是记录三个时间戳[82]。

1. “[Windowing (Azure Stream Analytics)](https://msdn.microsoft.com/en-us/library/azure/dn835019.aspx),” Microsoft Azure Reference, *msdn.microsoft.com*, April 2016.

      > 一旦你知道应该如何确定一个事件的时间戳，下一步就是决定如何定义时间段的窗口。然后，窗口可以用于聚合，例如计算事件，或计算窗口内数值的平均值。有几种类型的窗口被普遍使用[79, 83]。

1. “[State Management](http://samza.apache.org/learn/documentation/0.10/container/state-management.html),” Apache Samza 0.10 Documentation, *samza.apache.org*, December 2015.

      > 然而，新的事件可以随时出现在流中，这使得流中的连接比批处理作业中的连接更具挑战性。为了更好地理解这种情况，让我们区分三种不同类型的连接：流-流连接，流-表连接，以及表-表连接[84]。在下面的章节中，我们将通过例子来说明每一种类型。

1. Rajagopal Ananthanarayanan,
      Venkatesh Basker, Sumit Das, et al.:
      “[Photon: Fault-Tolerant and Scalable Joining of Continuous Data Streams](http://research.google.com/pubs/pub41318.html),” at *ACM International Conference on Management of
      Data* (SIGMOD), June 2013.
      [doi:10.1145/2463676.2465272](http://dx.doi.org/10.1145/2463676.2465272)

      > 假设你在你的网站上有一个搜索功能，你想检测最近搜索到的URL的趋势。每次有人输入一个搜索查询，你就记录一个包含查询和返回结果的事件。每次有人点击其中一个搜索结果，你就会记录另一个事件，记录这次点击。为了计算搜索结果中每个URL的点击率，你需要把搜索行为和点击行为的事件结合起来，这些事件通过相同的会话ID联系起来。在广告系统中也需要类似的分析[85]。

1. Martin Kleppmann:
      “[Samza Newsfeed Demo](https://github.com/ept/newsfeed),” *github.com*,
      September 2014.

      > 为了在流处理器中实现这种缓存维护，你需要为推文（发送和删除）和关注关系（关注和取消关注）提供事件流。流处理器需要维护一个包含每个用户的关注者集合的数据库，这样它就知道当一条新的推文到来时，哪些时间线需要被更新[86]。

1. Ben Kirwin:
      “[Doing the Impossible: Exactly-Once Messaging Patterns in Kafka](http://ben.kirw.in/2014/11/28/kafka-patterns/),” *ben.kirw.in*, November 28, 2014.

      > 如果事件在流中的排序是不确定的，那么连接就变成了非确定性的[87]，这意味着你不能在相同的输入上重新运行相同的作业，并且一定会得到相同的结果：当你再次运行作业时，输入流上的事件可能会以不同的方式交错进行。

1. Pat Helland:
      “[Data on the Outside Versus Data on the Inside](http://cidrdb.org/cidr2005/papers/P12.pdf),” at *2nd Biennial Conference on Innovative Data Systems Research* (CIDR), January
      2005.

1. Ralph Kimball and Margy Ross:
      *The Data Warehouse Toolkit: The Definitive Guide to Dimensional Modeling*,
      3rd edition. John Wiley & Sons, 2013. ISBN: 978-1-118-53080-1

      > 在数据仓库中，这个问题被称为缓慢变化的维度（SCD），它通常是通过对连接记录的特定版本使用唯一的标识符来解决的：例如，每次税率变化时，它都被赋予一个新的标识符，而发票中包括销售时的税率标识符[88, 89]。这种变化使连接具有确定性，但其后果是，日志压缩是不可能的，因为表中所有版本的记录都需要保留。

1. Viktor Klang:
      “[I'm coining the phrase 'effectively-once' for message processing with at-least-once + idempotent operations](https://twitter.com/viktorklang/status/789036133434978304),”
      *twitter.com*, October 20, 2016.

      > 特别是，批处理的容错方法确保了批处理作业的输出与没有出错的情况相同，即使事实上有些任务确实失败了。看起来好像每条输入记录都被精确地处理了一次--没有记录被跳过，也没有记录被处理两次。尽管重启任务意味着记录实际上可能被多次处理，但在输出中的可见效果就好像它们只被处理了一次。这一原则被称为 "完全一次性语义"，尽管 "有效一次性 "是一个更具描述性的术语[90]。

1. Matei Zaharia, Tathagata Das, Haoyuan Li, et al.:
      “[Discretized Streams: An Efficient and Fault-Tolerant Model for Stream Processing on Large Clusters](https://www.usenix.org/system/files/conference/hotcloud12/hotcloud12-final28.pdf),” at
      *4th USENIX Conference in Hot Topics in Cloud Computing* (HotCloud), June 2012.

      > 一种解决方案是将流分解成小块，并将每个块当作一个微型的批处理过程。这种方法被称为微批处理，它被用于Spark Streaming[91]。批量大小通常在一秒左右，这是性能折衷的结果：较小的批次会招致更大的调度和协调开销，而较大的批次意味着在流处理器的结果变得可见之前会有更长的延迟。

1. Kostas Tzoumas, Stephan Ewen, and Robert Metzger:
      “[High-Throughput, Low-Latency, and Exactly-Once Stream Processing with Apache Flink](https://www.ververica.com/blog/high-throughput-low-latency-and-exactly-once-stream-processing-with-apache-flink),”
      *ververica.com*, August 5, 2015.

1. Paris Carbone, Gyula Fóra, Stephan Ewen, et al.:
      “[Lightweight Asynchronous Snapshots for Distributed Dataflows](http://arxiv.org/abs/1506.08603),” arXiv:1506.08603 &#91;cs.DC&#93;, June 29, 2015.

      > Apache Flink中使用的另一种方法是定期生成状态的滚动检查点，并将其写入持久存储中[92, 93]。如果一个流运营商崩溃了，它可以从最近的检查点重新开始，并丢弃最后一个检查点和崩溃之间产生的任何输出。检查点是由消息流中的障碍物触发的，类似于微批之间的界限，但没有强制要求特定的窗口大小。

1. Ryan Betts and John Hugg:
      [*Fast Data: Smart and at Scale*](http://www.oreilly.com/data/free/fast-data-smart-and-at-scale.csp).
      Report, O'Reilly Media, October 2015.

1. Flavio Junqueira:
      “[Making Sense of Exactly-Once Semantics](http://conferences.oreilly.com/strata/hadoop-big-data-eu/public/schedule/detail/49690),” at *Strata+Hadoop World London*, June 2016.

1. Jason Gustafson, Flavio Junqueira, Apurva Mehta, Sriram Subramanian, and Guozhang Wang: “[KIP-98 – Exactly Once Delivery and Transactional Messaging](https://cwiki.apache.org/confluence/display/KAFKA/KIP-98+-+Exactly+Once+Delivery+and+Transactional+Messaging),” *cwiki.apache.org*, November 2016.

      > 在第9章中，我们讨论了分布式事务的传统实现中的问题，比如XA。然而，在更受限制的环境中，有可能有效地实现这样一个原子提交设施。这种方法在Google Cloud Dataflow[81, 92]和VoltDB[94]中使用，并且有计划在Apache Kafka[95, 96]中增加类似的功能。与XA不同的是，这些实现并不试图提供跨异构技术的交易，而是通过在流处理框架内管理状态变化和消息传递来保持其内部。交易协议的开销可以通过在一个交易中处理几个输入消息来分摊。

1. Pat Helland:
      “[Idempotence Is Not a Medical Condition](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.401.1539&rep=rep1&type=pdf),” *Communications of the ACM*, volume 55, number 5, page 56, May 2012.
      [doi:10.1145/2160718.2160734](http://dx.doi.org/10.1145/2160718.2160734)

      > 我们的目标是丢弃任何失败的任务的部分输出，以便它们可以安全地重试而不产生两次效果。分布式事务是实现这一目标的一种方式，但另一种方式是依靠空位[97]。

1. Jay Kreps:
      “[Re: Trying to Achieve Deterministic Behavior on Recovery/Rewind](http://mail-archives.apache.org/mod_mbox/samza-dev/201409.mbox/%3CCAOeJiJg%2Bc7Ei%3DgzCuOz30DD3G5Hm9yFY%3DUJ6SafdNUFbvRgorg%40mail.gmail.com%3E),” email to *samza-dev* mailing list,
      September 9, 2014.

1. E. N. (Mootaz) Elnozahy,
      Lorenzo Alvisi, Yi-Min Wang, and David B. Johnson:
      “[A Survey of Rollback-Recovery Protocols in Message-Passing Systems](http://www.cs.utexas.edu/~lorenzo/papers/SurveyFinal.pdf),” *ACM Computing Surveys*, volume 34, number 3,
      pages 375–408, September 2002.
      [doi:10.1145/568522.568525](http://dx.doi.org/10.1145/568522.568525)

      > Storm的Trident中的状态处理是基于一个类似的想法[78]。依靠idempotence意味着几个假设：重新启动一个失败的任务必须以相同的顺序重放相同的消息（基于日志的消息代理会这样做），处理必须是确定性的，并且没有其他节点可以同时更新相同的值[98, 99]。

1. Adam Warski:
      “[Kafka Streams – How Does It Fit the Stream Processing Landscape?](https://softwaremill.com/kafka-streams-how-does-it-fit-stream-landscape/),” *softwaremill.com*, June 1, 2016.

      > 例如，Flink定期捕获操作者状态的快照，并将其写入HDFS等持久性存储中[92, 93]；Samza和Kafka Streams通过将其发送到具有日志压缩功能的专用Kafka主题来复制状态变化，类似于变化数据捕获[84, 100]。VoltDB通过在几个节点上冗余地处理每个输入消息来复制状态（见 "实际串行执行"）。

