Designing Data-Intensive Applications
=====================================

Chapter 12 The Future of Data Systems
--------------------

1. Rachid Belaid:
    “[Postgres Full-Text Search is Good Enough!](http://rachbelaid.com/postgres-full-text-search-is-good-enough/),” *rachbelaid.com*, July 13, 2015.

    > 虽然有些数据库（如 postgreSQL）支持全文索引功能，可以满足一些简单应用[1]，但更复杂的查询则需要专业的信息检索工具

1. Philippe Ajoux, Nathan Bronson, Sanjeev Kumar, et al.:
    “[Challenges to Adopting Stronger Consistency at Scale](https://www.usenix.org/system/files/conference/hotos15/hotos15-paper-ajoux.pdf),” at *15th USENIX Workshop on Hot Topics
    in Operating Systems* (HotOS), May 2015.

1. Pat Helland and Dave Campbell:
    “[Building on Quicksand](https://database.cs.wisc.edu/cidr/cidr2009/Paper_133.pdf),” at
    *4th Biennial Conference on Innovative Data Systems Research* (CIDR), January 2009.

    > 排序事件以捕获因果关系
    >
    > ……不幸的是，似乎这个问题并没有一个简单的答案[2，3]

1. Jessica Kerr:
      “[Provenance   and Causality in Distributed Systems](https://web.archive.org/web/20190425150540/http://blog.jessitron.com/2016/09/provenance-and-causality-in-distributed.html),”
      *blog.jessitron.com*, September 25, 2016.

      > 排序事件以捕获因果关系
      >
      > ……如果可以记录一条时间来标记用户在做决定以前所看到的系统状态，并给该事件一个唯一的标识符，那么后续的事件都可以引用该事件标识符来记录因果关系

1. Kostas Tzoumas:
    “[Batch Is a Special Case of Streaming](http://data-artisans.com/batch-is-a-special-case-of-streaming/),” *data-artisans.com*, September 15, 2015.

    > 批处理和流处理集成
    >
    > ……Apache Flink 则直接在流处理引擎上执行批处理

1. Shinji Kim and Robert Blafford:
    “[Stream Windowing Performance Analysis: Concord and Spark Streaming](https://web.archive.org/web/20180125074821/http://concord.io/posts/windowing_performance_analysis_w_spark_streaming),”
    *concord.io*, July 6, 2016.

    > 批处理和流处理集成
    >
    > ……微批处理可能在跳跃或划动窗口上表现不佳

1. Jay Kreps:
    “[The Log: What Every Software Engineer Should Know About Real-Time Data's Unifying Abstraction](http://engineering.linkedin.com/distributed-systems/log-what-every-software-engineer-should-know-about-real-time-datas-unifying),”
    *engineering.linkedin.com*, December 16, 2013.

    > 保持派生状态
    >
    > ……具有良好定义的输入和输出的确定性函数原理上不仅有利于容错，而且还简化了组织中数据流的推理

1. Pat Helland:
    “[Life Beyond Distributed Transactions: An Apostate’s Opinion](http://www-db.cs.wisc.edu/cidr/cidr2007/papers/cidr07p15.pdf),” at *3rd Biennial Conference on Innovative Data
    Systems Research* (CIDR), January 2007.

    > 保持派生状态
    >
    > ……如果索引是异步维护的，这种交叉分区通信也是最可靠的最易扩展的

1. “[Great Western Railway (1835–1948)](https://web.archive.org/web/20160122155425/https://www.networkrail.co.uk/VirtualArchive/great-western/),”
    Network Rail Virtual Archive, *networkrail.co.uk*.

    > 发生在铁路上的模式迁移
    >
    > ……某一个尺寸标准而建的列车无法在另一个尺寸标准的轨道上运行，这严重限制了铁路网络大规模互连

1. Jacqueline Xu:
    “[Online Migrations at Scale](https://stripe.com/blog/online-migrations),”
    *stripe.com*, February 2, 2017.

    > 为应用程序演化而重新处理数据
    >
    > ……之后，逐渐增加访问新视图的用户比例，最终放弃旧视图

1. Molly Bartlett Dishman and Martin Fowler:
      “[Agile Architecture](http://conferences.oreilly.com/software-architecture/sa2015/public/schedule/detail/40388),” at *O'Reilly Software Architecture Conference*, March 2015.

      > 为应用程序演化而重新处理数据
      >
      > ……这种逐渐迁移的美妙之处，如果出现问题，每个阶段的过程都是可以轻易反转：你总是有一个工作系统可以回退。通过减少不可逆损害的风险，可以更加自信的向前推进，从而更快地改善系统

1. Nathan Marz and James Warren:
      [*Big Data: Principles and Best Practices of Scalable Real-Time Data Systems*](https://www.manning.com/books/big-data).
      Manning, 2015. ISBN: 978-1-617-29034-3

      > Lambda 架构
      >
      > ……如果批处理被用来重新处理历史数据，而流处理被用来处理最近的更新，那么如何将这两者结合起来？lambda架构[12]是这个领域的一个提议，已经获得了很多关注。

1. Oscar Boykin, Sam Ritchie, Ian O'Connell, and
      Jimmy Lin: “[Summingbird: A Framework for   Integrating Batch and Online MapReduce Computations](http://www.vldb.org/pvldb/vol7/p1441-boykin.pdf),” at *40th International Conference on
      Very Large Data Bases* (VLDB), September 2014.

1. Jay Kreps:
      “[Questioning the   Lambda Architecture](https://www.oreilly.com/ideas/questioning-the-lambda-architecture),” *oreilly.com*, July 2, 2014.

      >  在批处理和流处理框架中都要维护相同的逻辑，这是很重要的额外工作。尽管像Summingbird[13]这样的库为可以在批处理或流处理环境中运行的计算提供了一个抽象，但调试、调整和维护两个不同系统的操作复杂性仍然存在[14]。

1. Raul Castro Fernandez, Peter Pietzuch, Jay Kreps, et al.:
      “[Liquid: Unifying Nearline and Offline Big Data Integration](http://cidrdb.org/cidr2015/Papers/CIDR15_Paper25u.pdf),”
      at *7th Biennial Conference on Innovative Data Systems Research* (CIDR), January 2015.

      > 最近的工作使lambda架构的好处得以享受，而没有它的缺点，因为它允许在同一个系统中实现批量计算（重新处理历史数据）和流计算（在事件到来时处理）[15]。

1. Dennis M. Ritchie and Ken Thompson:
      “[The UNIX Time-Sharing System](http://web.eecs.utk.edu/~qcao1/cs560/papers/paper-unix.pdf),”
      *Communications of the ACM*, volume 17, number 7, pages 365–375, July 1974.
      [doi:10.1145/361011.361061](http://dx.doi.org/10.1145/361011.361061)

1. Eric A. Brewer and Joseph M. Hellerstein:
      “[CS262a: Advanced Topics in Computer Systems](http://people.eecs.berkeley.edu/~brewer/cs262/systemr.html),” lecture notes, University of California, Berkeley, *cs.berkeley.edu*,
      August 2011.

      > 在最抽象的层面上，数据库、Hadoop和操作系统都执行相同的功能：它们存储一些数据，并允许你处理和查询这些数据[16]。数据库将数据存储在一些数据模型的记录中（表格中的行、文件、图中的顶点等），而操作系统的文件系统将数据存储在文件中，但在其核心，两者都是 "信息管理 "系统[17]。正如我们在第10章中所看到的，Hadoop生态系统有点像一个分布式的Unix版本。

1. Michael Stonebraker:
      “[The Case for Polystores](http://wp.sigmod.org/?p=1629),” *wp.sigmod.org*,
      July 13, 2015.

1. Jennie Duggan,
      Aaron J. Elmore, Michael Stonebraker, et al.:
      “[The BigDAWG Polystore   System](http://dspace.mit.edu/openaccess-disseminate/1721.1/100936),” *ACM SIGMOD Record*, volume 44, number 2, pages 11–16, June 2015.
      [doi:10.1145/2814710.2814713](http://dx.doi.org/10.1145/2814710.2814713)

1. Patrycja Dybka:
      “[Foreign   Data Wrappers for PostgreSQL](http://www.vertabelo.com/blog/technical-articles/foreign-data-wrappers-for-postgresql),” *vertabelo.com*, March 24, 2015.

      > 有可能为各种各样的底层存储引擎和处理方法提供一个统一的查询接口--这种方法被称为联合数据库或多库[18, 19]。例如，PostgreSQL的外来数据封装功能符合这种模式[20]。需要专门的数据模型或查询接口的应用程序仍然可以直接访问底层的存储引擎，而想要结合来自不同地方的数据的用户可以通过联合接口轻松实现。

1. David B. Lomet, Alan Fekete, Gerhard Weikum, and Mike Zwilling:
      “[Unbundling   Transaction Services in the Cloud](https://www.microsoft.com/en-us/research/publication/unbundling-transaction-services-in-the-cloud/),” at *4th Biennial Conference on Innovative Data Systems
      Research* (CIDR), January 2009.

      > 虽然联邦解决了跨几个不同系统的只读查询，但它对跨这些系统的同步写入没有一个很好的答案。我们说过，在一个单一的数据库内，创建一个一致的索引是一个内置的功能。当我们组成几个存储系统时，我们同样需要确保所有的数据变化最终都出现在所有正确的地方，即使面对故障。使得可靠地将存储系统连接在一起变得更加容易（例如，通过变化数据捕获和事件日志），就像将数据库的索引维护功能解绑一样，可以在不同的技术之间同步写入[7, 21]。

1. Martin Kleppmann and Jay Kreps:
      “[Kafka, Samza and the Unix Philosophy of Distributed Data](http://martin.kleppmann.com/papers/kafka-debull15.pdf),” *IEEE Data Engineering Bulletin*, volume 38, number 4, pages 4–14,
      December 2015.

      > 非捆绑式方法遵循Unix的传统，即做一件事做得好的小工具[22]，通过统一的低级API（管道）进行通信，并可使用高级语言（shell）进行组合[16]。

1. John Hugg:
      “[Winning Now and in the Future: Where VoltDB Shines](https://voltdb.com/blog/winning-now-and-future-where-voltdb-shines),” *voltdb.com*, March 23, 2016.

      > 运行几个不同的基础设施的复杂性可能是一个问题：每个软件都有一个学习曲线、配置问题和操作怪癖，因此值得部署尽可能少的移动部件。与一个由你用应用程序代码组成的几个工具组成的系统相比，一个单一的集成软件产品可能还能在它所设计的那种工作负载上取得更好、更可预测的性能[23]。正如我在序言中所说，为你不需要的规模而构建是浪费精力的，而且可能会把你锁定在一个不灵活的设计中。实际上，这是一种不成熟的优化形式。

1. Frank McSherry, Derek G. Murray, Rebecca Isaacs, and Michael Isard:
      “[Differential Dataflow](http://cidrdb.org/cidr2013/Papers/CIDR13_Paper111.pdf),”
      at *6th Biennial Conference on Innovative Data Systems Research* (CIDR), January 2013.

      > 

1. Derek G Murray, Frank McSherry, Rebecca Isaacs, et al.:
      “[Naiad: A Timely Dataflow System](http://sigops.org/s/conferences/sosp/2013/papers/p439-murray.pdf),”
      at *24th ACM Symposium on Operating Systems Principles* (SOSP), pages 439–455, November 2013.
      [doi:10.1145/2517349.2522738](http://dx.doi.org/10.1145/2517349.2522738)

      > 同样的，如果能够更容易地预计算和更新缓存，那就更好了。回顾一下，物化视图本质上是一个预计算的缓存，所以你可以想象通过声明地指定复杂查询的物化视图来创建一个缓存，包括对图的递归查询（见 "类似图的数据模型"）和应用逻辑。在这个领域有一些有趣的早期研究，比如差分数据流[24, 25]，我希望这些想法能在生产系统中找到它们的方法。

1. Gwen Shapira:
      “[We have a bunch of customers who are implementing ‘database inside-out’ concept and they all ask ‘is anyone else doing it? are we crazy?’](https://twitter.com/gwenshap/status/758800071110430720)” *twitter.com*, July 28, 2016.

1. Martin Kleppmann:
      “[Turning the Database Inside-out with Apache Samza,](http://martin.kleppmann.com/2015/03/04/turning-the-database-inside-out.html)” at *Strange Loop*, September 2014.

      > 通过将专门的存储和处理系统与应用程序代码相结合来解开数据库的方法也逐渐被称为 "数据库由内向外 "的方法[26]，这是我在2014年发表的一个会议演讲的标题[27]。然而，称其为 "新架构 "未免过于宏大。我认为它更像是一种设计模式，一个讨论的起点，我们给它一个名字只是为了让我们能更好地谈论它。

1. Peter Van Roy and Seif Haridi:
      [*Concepts, Techniques, and Models of Computer Programming*](https://www.info.ucl.ac.be/~pvr/book.html).
      MIT Press, 2004. ISBN: 978-0-262-22069-9

1. “[Juttle Documentation](http://juttle.github.io/juttle/),” *juttle.github.io*, 2016.

1. Evan Czaplicki and Stephen Chong:
      “[Asynchronous Functional Reactive Programming for GUIs](http://people.seas.harvard.edu/~chong/pubs/pldi13-elm.pdf),” at *34th ACM SIGPLAN Conference on Programming Language
      Design and Implementation* (PLDI), June 2013.
      [doi:10.1145/2491956.2462161](http://dx.doi.org/10.1145/2491956.2462161)

1. Engineer Bainomugisha, Andoni Lombide Carreton,
      Tom van Cutsem, Stijn Mostinckx, and Wolfgang de Meuter:
      “[A Survey on Reactive Programming](http://soft.vub.ac.be/Publications/2012/vub-soft-tr-12-13.pdf),” *ACM Computing Surveys*, volume 45, number 4, pages 1–34, August 2013.
      [doi:10.1145/2501654.2501666](http://dx.doi.org/10.1145/2501654.2501666)

1. Peter Alvaro, Neil Conway, Joseph M. Hellerstein, and William R. Marczak:
      “[Consistency Analysis in Bloom: A CALM and Collected Approach](https://dsf.berkeley.edu/cs286/papers/calm-cidr2011.pdf),”
      at *5th Biennial Conference on Innovative Data Systems Research* (CIDR), January 2011.

      > 这些想法不是我的；它们只是其他人的想法的混合体，我认为我们应该从中学习。特别是与Oz[28]和Juttle[29]等数据流语言、Elm[30, 31]等函数式反应编程（FRP）语言以及Bloom[32]等逻辑编程语言有很多重合。这方面的术语unbundling是由Jay Kreps[7]提出的。

1. Felienne Hermans:
      “[Spreadsheets Are Code](https://vimeo.com/145492419),” at *Code Mesh*, November 2015.

      > 甚至电子表格也有数据流编程功能，比大多数主流编程语言要领先许多[33]。在电子表格中，你可以把一个公式放在一个单元格中（例如，另一列的单元格之和），每当公式的任何输入发生变化，公式的结果就会自动重新计算。这正是我们在数据系统层面所希望的：当数据库中的一条记录发生变化时，我们希望该记录的任何索引都能自动更新，任何依赖该记录的缓存视图或聚合都能自动刷新。你不应该担心这种刷新是如何发生的技术细节，而应该能够简单地相信它是正确工作的。

1. Dan Bricklin and Bob
      Frankston: “[VisiCalc: Information from Its Creators](http://danbricklin.com/visicalc.htm),” *danbricklin.com*.

      > 因此，我认为大多数数据系统仍然可以从VisiCalc在1979年已经拥有的功能中学习到一些东西[34]。与电子表格不同的是，今天的数据系统需要具有容错性、可扩展性，并能持久地存储数据。它们还需要能够整合由不同人群长期编写的不同技术，并重用现有的库和服务：期望所有的软件都使用一种特定的语言、框架或工具来开发是不现实的。

1. D. Sculley, Gary Holt, Daniel Golovin, et al.:
      “[Machine Learning: The High-Interest Credit Card of Technical Debt](http://research.google.com/pubs/pub43146.html),” at *NIPS Workshop on Software Engineering for Machine Learning*
      (SE4ML), December 2014.

1. Peter Bailis, Alan Fekete, Michael J Franklin,
      et al.: “[Feral Concurrency Control: An Empirical Investigation of Modern Application Integrity](http://www.bailis.org/papers/feral-sigmod2015.pdf),” at *ACM International Conference on
      Management of Data* (SIGMOD), June 2015.
      [doi:10.1145/2723372.2737784](http://dx.doi.org/10.1145/2723372.2737784)

1. Guy Steele:
      “[Re: Need for Macros (Was Re: Icon)](https://people.csail.mit.edu/gregs/ll1-discuss-archive-html/msg01134.html),” email to *ll1-discuss* mailing list, *people.csail.mit.edu*, December 24,
      2001.

      > 今天，大多数网络应用程序被部署为无状态服务，在这种情况下，任何用户请求都可以被路由到任何应用服务器，而服务器一旦发出响应就会忘记关于请求的一切。这种部署方式很方便，因为服务器可以随意添加或删除，但状态必须要有一个地方：通常是一个数据库。现在的趋势是将无状态的应用逻辑与状态管理（数据库）分开：不把应用逻辑放在数据库中，也不把持久性状态放在应用中[36]。正如函数式编程社区的人们喜欢开玩笑的那样，"我们相信Church和state的分离"[37]

1. David Gelernter:
      “[Generative Communication in Linda](http://cseweb.ucsd.edu/groups/csag/html/teaching/cse291s03/Readings/p80-gelernter.pdf),” *ACM Transactions on Programming Languages and Systems*
      (TOPLAS), volume 7, number 1, pages 80–112, January 1985.
      [doi:10.1145/2363.2433](http://dx.doi.org/10.1145/2363.2433)

1. Patrick Th. Eugster, Pascal A. Felber,
      Rachid Guerraoui, and Anne-Marie Kermarrec:
      “[The Many Faces of Publish/Subscribe](http://www.cs.ru.nl/~pieter/oss/manyfaces.pdf),”
      *ACM Computing Surveys*, volume 35, number 2, pages 114–131, June 2003.
      [doi:10.1145/857076.857078](http://dx.doi.org/10.1145/857076.857078)

      > 我们在 "数据库和流 "中看到了这种思路，在那里我们讨论了将数据库的变化日志视为我们可以订阅的事件流。消息传递系统，如行动者（见 "消息传递数据流"）也有这种对事件做出反应的概念。早在20世纪80年代，元组空间模型就探索了用观察状态变化并对其做出反应的过程来表达分布式计算[38, 39]。

1. Ben Stopford:
      “[Microservices in a Streaming World](https://www.infoq.com/presentations/microservices-streaming),” at *QCon London*, March 2016.

      > 将流操作者组成数据流系统，与微服务方法[40]有很多类似的特点。然而，底层的通信机制是非常不同的：单向的、异步的消息流，而不是同步的请求/响应的互动。

1. Christian Posta:
      “[Why Microservices Should Be Event Driven: Autonomy vs Authority](http://blog.christianposta.com/microservices/why-microservices-should-be-event-driven-autonomy-vs-authority/),” *blog.christianposta.com*, May 27, 2016.

      > 除了 "消息传递数据流 "中列出的优点，如更好的容错性，数据流系统还可以实现更好的性能。例如，假设一个客户要购买一个以一种货币定价但以另一种货币支付的商品。为了进行货币转换，你需要知道当前的汇率。这个操作可以通过两种方式实现[40, 41]。

1. Alex Feyerke:
      “[Say Hello to Offline First](http://hood.ie/blog/say-hello-to-offline-first.html),”
      *hood.ie*, November 5, 2013.

      > 这些不断变化的能力使人们对离线优先的应用程序重新产生兴趣，这些应用程序尽可能使用同一设备上的本地数据库，不需要互联网连接，当有网络连接时，在后台与远程服务器进行同步[42]。由于移动设备经常有缓慢和不可靠的蜂窝网络连接，如果他们的用户界面不需要等待同步的网络请求，如果应用程序大多是离线工作，这对用户来说是一个很大的优势（见 "离线操作的客户端"）。

1. Sebastian Burckhardt, Daan Leijen, Jonathan
      Protzenko, and Manuel Fähndrich:
      “[Global Sequence Protocol: A Robust Abstraction for Replicated Shared State](http://drops.dagstuhl.de/opus/volltexte/2015/5238/),” at *29th European Conference on Object-Oriented
      Programming* (ECOOP), July 2015.
      [doi:10.4230/LIPIcs.ECOOP.2015.568](http://dx.doi.org/10.4230/LIPIcs.ECOOP.2015.568)

      > 就我们的写路径和读路径模型而言，积极地将状态变化一直推送到客户端设备，意味着将写路径一直延伸到终端用户。当客户端第一次被初始化时，它仍然需要使用读取路径来获得其初始状态，但此后它可以依赖服务器发送的状态变化流。我们讨论的围绕流处理和消息传递的想法并不局限于只在数据中心运行：我们可以进一步发挥这些想法，并将其一直延伸到最终用户设备[43]。

1. Mark Soper:
      “[Clearing Up React Data Management Confusion with Flux, Redux, and Relay](https://medium.com/@marksoper/clearing-up-react-data-management-confusion-with-flux-redux-and-relay-aad504e63cae),” *medium.com*, December 3, 2015.

1. Eno Thereska, Damian Guy, Michael Noll, and Neha Narkhede:
      “[Unifying Stream Processing and Interactive Queries in Apache Kafka](http://www.confluent.io/blog/unifying-stream-processing-and-interactive-queries-in-apache-kafka/),” *confluent.io*, October 26, 2016.

      > 在许多情况下，数据存储与流系统是分开的。但是回顾一下，流处理器也需要维护状态以执行聚合和连接（见 "流连接"）。这种状态通常隐藏在流处理器内部，但有些框架允许外部客户查询它[45]，把流处理器本身变成一种简单的数据库。

1. Frank McSherry:
      “[Dataflow as Database](https://github.com/frankmcsherry/blog/blob/master/posts/2016-07-17.md),” *github.com*, July 17, 2016.

      > 我想进一步发挥这个想法。正如到目前为止所讨论的，对存储的写入要通过事件日志，而读取则是瞬时的网络请求，直接进入存储被查询数据的节点。这是一个合理的设计，但不是唯一可能的设计。也可以把读取请求表示为事件流，并通过流处理器发送读取事件和写入事件；处理器对读取事件的反应是把读取的结果发送到输出流[46]。

1. Peter Alvaro:
      “[I See What You Mean](https://www.youtube.com/watch?v=R2Aa4PivG0g),” at *Strange
      Loop*, September 2015.

1. Nathan Marz:
      “[Trident: A High-Level Abstraction for Realtime Computation](https://blog.twitter.com/2012/trident-a-high-level-abstraction-for-realtime-computation),” *blog.twitter.com*, August 2, 2012.

      > Storm的分布式RPC功能支持这种使用模式（见 "消息传递和RPC"）。例如，它已经被用来计算在Twitter上看到一个URL的人数--即在推特上发布过该URL的每个人的粉丝集的联合[48]。由于Twitter用户的集合是分区的，这种计算需要结合许多分区的结果。

1. Edi Bice:
      “[Low Latency Web Scale Fraud Prevention with Apache Samza, Kafka and Friends](http://www.slideshare.net/edibice/extremely-low-latency-web-scale-fraud-prevention-with-apache-samza-kafka-and-friends),” at *Merchant Risk
      Council MRC Vegas Conference*, March 2016.

      > 这种模式的另一个例子发生在防欺诈中：为了评估某个特定的购买事件是否有欺诈行为的风险，你可以检查用户的IP地址、电子邮件地址、账单地址、送货地址等的信誉分数。这些信誉数据库中的每一个本身都是分区的，因此收集特定购买事件的分数需要与不同分区的数据集进行一系列的连接[49]。

1. Charity Majors:
      “[The Accidental DBA](https://charity.wtf/2016/10/02/the-accidental-dba/),” *charity.wtf*,
      October 2, 2016.

      > 对于只读数据的无状态服务，如果出了问题也不是什么大问题：你可以修复错误并重新启动服务，一切都会恢复正常。数据库等有状态的系统就不那么简单了：它们被设计成永远记住东西（或多或少），所以如果出了问题，其影响也可能永远持续下去--这意味着它们需要更仔细的思考[50]。

1. Arthur J. Bernstein, Philip M. Lewis, and Shiyong Lu:
      “[Semantic Conditions for Correctness at Different Isolation Levels](http://db.cs.berkeley.edu/cs286/papers/isolation-icde2000.pdf),” at *16th International Conference on Data
      Engineering* (ICDE), February 2000.
      [doi:10.1109/ICDE.2000.839387](http://dx.doi.org/10.1109/ICDE.2000.839387)

1. Sudhir Jorwekar, Alan Fekete, Krithi Ramamritham, and
      S. Sudarshan: “[Automating the Detection of Snapshot Isolation Anomalies](http://www.vldb.org/conf/2007/papers/industrial/p1263-jorwekar.pdf),” at *33rd International Conference on Very
      Large Data Bases* (VLDB), September 2007.

      > 对于一个如此重要的话题，我们的理解和我们的工程方法却出乎意料的飘忽。例如，要确定在一个特定的事务隔离级别或复制配置下运行一个特定的应用程序是否安全是非常困难的[51, 52]。通常情况下，简单的解决方案在并发性低且没有故障的情况下似乎可以正常工作，但在要求更高的情况下却发现有许多微妙的错误。

1. Kyle Kingsbury:
      [Jepsen blog post series](https://aphyr.com/tags/jepsen), *aphyr.com*, 2013–2016.

1. Michael Jouravlev:
      “[Redirect After Post](http://www.theserverside.com/news/1365146/Redirect-After-Post),”
      *theserverside.com*, August 1, 2004.

      > 在这种情况下，用户可能会看到一个错误信息，他们可能会手动重试。网络浏览器会警告说："你确定要再次提交这个表单吗？"--用户会说是的，因为他们想让这个操作发生。(Post/Redirect/Get模式[54]在正常操作中避免了这种警告信息，但如果POST请求超时，它也无济于事。) 从Web服务器的角度来看，重试是一个单独的请求，而从数据库的角度来看，它是一个单独的事务。通常的重复数据删除机制并没有帮助。

1. Jerome H. Saltzer, David P. Reed, and David D. Clark:
      “[End-to-End Arguments in System Design](https://groups.csail.mit.edu/ana/Publications/PubPDFs/End-to-End%20Arguments%20in%20System%20Design.pdf),”
      *ACM Transactions on Computer Systems*, volume 2, number 4, pages 277–288, November 1984.
      [doi:10.1145/357401.357402](http://dx.doi.org/10.1145/357401.357402)

      > 类似的论点也适用于加密[55]：你家里WiFi网络的密码可以防止人们窥探你的WiFi流量，但不能防止互联网上其他地方的攻击者；你的客户端和服务器之间的TLS/SSL可以防止网络攻击者，但不能防止服务器的妥协。只有端到端的加密和认证才能防止所有这些事情。

1. Peter Bailis, Alan Fekete, Michael J. Franklin, et al.:
      “[Coordination-Avoiding Database Systems](http://arxiv.org/pdf/1402.2237.pdf),”
      *Proceedings of the VLDB Endowment*, volume 8, number 3, pages 185–196, November 2014.

1. Alex Yarmula:
      “[Strong Consistency in Manhattan](https://blog.twitter.com/2016/strong-consistency-in-manhattan),” *blog.twitter.com*, March 17, 2016.

      > 一个流处理器在一个单线程上按顺序消耗一个日志分区中的所有消息（见 "日志与传统消息传递的比较"）。因此，如果日志是根据需要唯一的值来划分的，那么流处理器可以毫不含糊地、确定地决定几个冲突的操作中哪一个先出现。例如，在几个用户试图索取同一个用户名的情况下[57]。

1. Douglas B Terry, Marvin M Theimer, Karin Petersen, et al.:
      “[Managing Update Conflicts in Bayou, a Weakly Connected Replicated Storage System](http://css.csail.mit.edu/6.824/2014/papers/bayou-conflicts.pdf),” at *15th ACM Symposium on Operating
      Systems Principles* (SOSP), pages 172–182, December 1995.
      [doi:10.1145/224056.224070](http://dx.doi.org/10.1145/224056.224070)

      > 该方法不仅适用于唯一性约束，也适用于许多其他类型的约束。它的基本原则是，任何可能发生冲突的写入都被路由到同一个分区，并按顺序处理。正如在 "什么是冲突？"和 "写偏移和幻影 "中所讨论的，冲突的定义可能取决于应用，但流处理器可以使用任意的逻辑来验证一个请求。这个想法类似于Bayou在90年代开创的方法[58]。

1. Jim Gray:
      “[The Transaction Concept: Virtues and Limitations](http://jimgray.azurewebsites.net/papers/thetransactionconcept.pdf),”
      at *7th International Conference on Very Large Data Bases* (VLDB), September 1981.

1. Hector Garcia-Molina and Kenneth Salem:
      “[Sagas](http://www.cs.cornell.edu/andru/cs711/2002fa/reading/sagas.pdf),” at
      *ACM International Conference on Management of Data* (SIGMOD), May 1987.
      [doi:10.1145/38713.38742](http://dx.doi.org/10.1145/38713.38742)

      >  如果两个人同时注册了相同的用户名或预订了相同的座位，你可以给其中一个人发信息表示歉意，并要求他们选择不同的座位。这种纠正错误的改变被称为补偿性交易[59, 60]。

1. Pat Helland:
      “[Memories, Guesses, and Apologies](https://web.archive.org/web/20160304020907/http://blogs.msdn.com/b/pathelland/archive/2007/05/15/memories-guesses-and-apologies.aspx),”
      *blogs.msdn.com*, May 15, 2007.

1. Yoongu Kim, Ross Daly, Jeremie Kim, et al.:
      “[Flipping Bits in Memory Without Accessing Them: An Experimental Study of DRAM Disturbance Errors](https://users.ece.cmu.edu/~yoonguk/papers/kim-isca14.pdf),” at *41st Annual
      International Symposium on Computer Architecture* (ISCA), June 2014.
      [doi:10.1145/2678373.2665726](http://dx.doi.org/10.1145/2678373.2665726)

      > 如果客户订购的物品比你仓库里的多，你可以订购更多的库存，为延误向客户道歉，并为他们提供折扣。这实际上和你要做的事情是一样的，比如说，一辆叉车碾压了你仓库里的一些物品，使你的库存比你认为的要少[61]。因此，无论如何，道歉工作流程已经需要成为你的业务流程的一部分，所以可能没有必要要求对库存物品的数量有一个可线性化的约束。

1. Mark Seaborn and Thomas Dullien:
      “[Exploiting the DRAM Rowhammer Bug to Gain Kernel Privileges](https://googleprojectzero.blogspot.co.uk/2015/03/exploiting-dram-rowhammer-bug-to-gain.html),” *googleprojectzero.blogspot.co.uk*, March 9,
      2015.

      > 我过去工作的一个应用程序从客户那里收集崩溃报告，而我们收到的一些报告只能用这些设备内存中的随机比特翻转来解释。这似乎不太可能，但如果你有足够的设备运行你的软件，即使是非常不可能的事情也会发生。除了硬件故障或辐射导致的随机内存损坏，某些病态的内存访问模式甚至可以在没有故障的内存中翻转比特[62]--这种效果可以用来破坏操作系统的安全机制[63]（这种技术被称为rowhammer）。一旦你仔细观察，硬件并不像它看起来那么完美的抽象。

1. Jim N. Gray and Catharine van Ingen:
      “[Empirical Measurements of Disk Failure Rates and Error Rates](https://www.microsoft.com/en-us/research/publication/empirical-measurements-of-disk-failure-rates-and-error-rates/),” Microsoft Research, MSR-TR-2005-166,
      December 2005.

      > 说白了，随机比特翻转在现代硬件上仍然非常罕见[64]。我只是想指出，它们并不是超出了可能性的范围，所以它们值得关注。

1. Annamalai Gurusami and Daniel Price:
      “[Bug #73170: Duplicates in Unique Secondary Index Because of Fix of Bug#68021](http://bugs.mysql.com/bug.php?id=73170),” *bugs.mysql.com*, July 2014.

1. Gary Fredericks:
      “[Postgres Serializability Bug](https://github.com/gfredericks/pg-serializability-bug),”
      *github.com*, September 2015.

      > 除了这样的硬件问题，还有软件错误的风险，这些错误不会被较低级别的网络、内存或文件系统检查所发现。即使是广泛使用的数据库软件也有错误。我曾亲眼见过MySQL无法正确维护唯一性约束的案例[65]，以及PostgreSQL的可序列化隔离级别表现出的写偏移异常[66]，尽管MySQL和PostgreSQL是经过许多人多年实战检验的强大且广受好评的数据库。在不太成熟的软件中，情况可能会更糟糕。

1. Xiao Chen:
      “[HDFS DataNode Scanners and Disk Checker Explained](http://blog.cloudera.com/blog/2016/12/hdfs-datanode-scanners-and-disk-checker-explained/),” *blog.cloudera.com*, December 20,
      2016.

      > 成熟的系统同样倾向于考虑不太可能出错的可能性，并管理这种风险。例如，像HDFS和Amazon S3这样的大规模存储系统并不完全信任磁盘：它们运行后台进程，不断地回读文件，将其与其他副本进行比较，并将文件从一个磁盘移到另一个磁盘，以减轻无声的损坏风险[67]。

1. Jay Kreps:
      “[Getting Real About Distributed System Reliability](http://blog.empathybox.com/post/19574936361/getting-real-about-distributed-system-reliability),” *blog.empathybox.com*, March 19, 2012.

      > 像HDFS和S3这样的系统仍然要假设磁盘在大多数时候都能正确工作，这是一个合理的假设，但不等于假设它们总是正确工作。然而，目前没有多少系统有这种 "信任，但要验证 "的方法，不断地审计自己。许多人假设正确性保证是绝对的，没有为罕见的数据损坏的可能性做出规定。我希望在未来我们能看到更多的自我验证或自我审计的系统，不断地检查自己的完整性，而不是依赖盲目的信任[68]。

1. Martin Fowler:
      “[The LMAX Architecture](http://martinfowler.com/articles/lmax.html),”
      *martinfowler.com*, July 12, 2011.

      > 一个确定的和定义良好的数据流也使得调试和跟踪系统的执行更加容易，以确定它为什么要做某些事情[4, 69]。如果发生了一些意外的事情，拥有重现导致意外事件发生的确切情况的诊断能力是很有价值的--一种时间旅行的调试能力。

1. Sam Stokes:
      “[Move Fast with Confidence](http://blog.samstokes.co.uk/blog/2016/07/11/move-fast-with-confidence/),” *blog.samstokes.co.uk*, July 11, 2016.

1. “[Hyperledger Sawtooth documentation](https://sawtooth.hyperledger.org/docs/core/releases/latest/introduction.html),”
      Intel Corporation, *sawtooth.hyperledger.org*, 2017.

1. Richard Gendal Brown:
      “[Introducing R3 Corda™: A Distributed Ledger Designed for Financial Services](https://gendal.me/2016/04/05/introducing-r3-corda-a-distributed-ledger-designed-for-financial-services/),” *gendal.me*, April 5, 2016.

1. Trent McConaghy, Rodolphe Marques, Andreas Müller, et al.:
      “[BigchainDB: A Scalable Blockchain Database](https://www.bigchaindb.com/whitepaper/bigchaindb-whitepaper.pdf),” *bigchaindb.com*, June 8, 2016.

      > 使用密码学工具来证明系统的完整性将是非常有趣的，这种方式对广泛的硬件和软件问题，甚至潜在的恶意行为都很稳健。加密货币、区块链和分布式账本技术，如比特币、以太坊、瑞波币、恒星币和其他各种技术[71, 72, 73]，已经涌现出探索这一领域。

1. Ralph C. Merkle:
      “[A Digital Signature Based on a Conventional Encryption Function](https://people.eecs.berkeley.edu/~raluca/cs261-f15/readings/merkle.pdf),” at *CRYPTO '87*, August 1987.
      [doi:10.1007/3-540-48184-2_32](http://dx.doi.org/10.1007/3-540-48184-2_32)

1. Ben Laurie:
      “[Certificate Transparency](http://queue.acm.org/detail.cfm?id=2668154),” *ACM
      Queue*, volume 12, number 8, pages 10-19, August 2014.
      [doi:10.1145/2668152.2668154](http://dx.doi.org/10.1145/2668152.2668154)

1. Mark D. Ryan:
      “[Enhanced Certificate Transparency and End-to-End Encrypted Mail](https://www.ndss-symposium.org/wp-content/uploads/2017/09/12_2_1.pdf),”
      at *Network and Distributed System Security Symposium* (NDSS), February 2014.
      [doi:10.14722/ndss.2014.23379](http://dx.doi.org/10.14722/ndss.2014.23379)

      > 加密审计和完整性检查经常依赖于Merkle树[74]，它是由哈希值组成的树，可以用来有效地证明一条记录出现在某些数据集中（以及其他一些东西）。在加密货币的炒作之外，证书透明度是一种安全技术，它依赖于Merkle树来检查TLS/SSL证书的有效性[75, 76]。

1. “[Software Engineering Code of Ethics and Professional Practice](http://www.acm.org/about/se-code),”
      Association for Computing Machinery, *acm.org*, 1999.

1. François Chollet:
      “[Software development is starting to involve important ethical choices](https://twitter.com/fchollet/status/792958695722201088),” *twitter.com*, October 30, 2016.

1. Igor Perisic:
      “[Making Hard Choices: The Quest for Ethics in Machine Learning](https://engineering.linkedin.com/blog/2016/11/making-hard-choices--the-quest-for-ethics-in-machine-learning),” *engineering.linkedin.com*, November
      2016.

1. John Naughton:
      “[Algorithm Writers Need a Code of Conduct](https://www.theguardian.com/commentisfree/2015/dec/06/algorithm-writers-should-have-code-of-conduct),” *theguardian.com*, December 6, 2015.

      > 软件开发越来越多地涉及到做出重要的伦理选择。有一些准则可以帮助软件工程师处理这些问题，比如ACM的《软件工程道德和专业实践准则》[77]，但这些准则在实践中很少被讨论、应用和执行。因此，工程师和产品经理有时对其产品的隐私和潜在的负面后果采取非常轻率的态度[78, 79, 80]。

1. Logan Kugler:
      “[What Happens When Big Data Blunders?](http://cacm.acm.org/magazines/2016/6/202655-what-happens-when-big-data-blunders/fulltext),” *Communications of the ACM*, volume 59, number 6, pages
      15–16, June 2016. [doi:10.1145/2911975](http://dx.doi.org/10.1145/2911975)

      > 例如，预测性分析是 "大数据 "炒作的一个主要部分。使用数据分析来预测天气或疾病的传播是一回事[81]；预测一个罪犯是否有可能重新犯罪，一个贷款申请人是否有可能违约，或者一个保险客户是否有可能提出昂贵的索赔是另一回事。后者对个人的生活有直接影响。

1. Bill Davidow:
      “[Welcome to Algorithmic Prison](http://www.theatlantic.com/technology/archive/2014/02/welcome-to-algorithmic-prison/283985/),” *theatlantic.com*, February 20, 2014.

      > 然而，随着算法决策变得越来越普遍，一个被某种算法（准确或错误地）贴上风险标签的人可能会遭受大量的这种 "不 "的决定。系统性地被排除在工作、航空旅行、保险、房产租赁、金融服务和社会其他关键方面之外，这是对个人自由的巨大限制，因此被称为 "算法监狱"[82]。在尊重人权的国家，刑事司法系统在被证明有罪之前是假定无罪的；另一方面，自动化系统可以在没有任何罪证的情况下系统地、任意地将一个人排除在社会参与之外，而且几乎没有上诉机会。

1. Don Peck:
      “[They're Watching You at Work](http://www.theatlantic.com/magazine/archive/2013/12/theyre-watching-you-at-work/354681/),” *theatlantic.com*, December 2013.

      > 算法作出的决定不一定比人作出的决定好或坏。每个人都可能有偏见，即使他们积极地试图抵制这些偏见，而且歧视性做法可能在文化上成为制度。人们希望将决定建立在数据上，而不是人的主观和本能的评估上，可以更加公平，给那些在传统系统中经常被忽视的人以更好的机会[83]。

1. Leigh Alexander:
      “[Is an Algorithm Any Less Racist Than a Human?](https://www.theguardian.com/technology/2016/aug/03/algorithm-racist-human-employers-work)” *theguardian.com*, August 3, 2016.

      > 当我们开发预测性分析系统时，我们不仅仅是通过使用软件来指定何时说 "是 "或 "不是 "的规则来实现人类决策的自动化；我们甚至让这些规则本身从数据中推断出来。然而，这些系统学到的模式是不透明的：即使数据中存在一些相关性，我们也可能不知道原因。如果一个算法的输入中存在系统性的偏见，那么该系统很可能会在其输出中学习并放大这种偏见[84]。

1. Jesse Emspak:
      “[How a Machine Learns Prejudice](https://www.scientificamerican.com/article/how-a-machine-learns-prejudice/),” *scientificamerican.com*, December 29, 2016.

1. Maciej Cegłowski:
      “[The Moral Economy of Tech](http://idlewords.com/talks/sase_panel.htm),”
      *idlewords.com*, June 2016.

      > 在许多国家，反歧视法禁止根据受保护的特征，如种族、年龄、性别、性、残疾或信仰，对人们进行区别对待。一个人的数据的其他特征可以被分析，但如果它们与受保护的特征相关，会发生什么？例如，在种族隔离的社区，一个人的邮政编码，甚至他们的IP地址都是一个强有力的种族预测因素。这样说来，相信一个算法可以以某种方式将有偏见的数据作为输入，并从中产生公平和公正的输出，似乎很荒谬[85]。然而，这种信念似乎常常被数据驱动决策的支持者所暗示，这种态度被讽刺为 "机器学习就像为偏见洗钱"[86]。

1. Cathy O'Neil:
      [*Weapons of Math Destruction: How Big Data Increases Inequality and Threatens Democracy*](https://weaponsofmathdestructionbook.com/).
      Crown Publishing, 2016. ISBN: 978-0-553-41881-1

      > 预测分析系统只是从过去推断；如果过去是歧视性的，它们就会把这种歧视编成法典。如果我们希望未来比过去更好，就需要道德上的想象力，而这是只有人类才能提供的东西[87]。数据和模型应该是我们的工具，而不是我们的主人。

1. Julia Angwin:
      “[Make Algorithms Accountable](http://www.nytimes.com/2016/08/01/opinion/make-algorithms-accountable.html),” *nytimes.com*, August 1, 2016.

      > 自动化决策开启了责任和问责的问题[87]。如果人类犯了错误，他们可以被追究责任，而受决策影响的人可以上诉。算法也会犯错，但如果它们出错，谁来负责[88]？当一辆自动驾驶汽车造成事故时，谁来负责？如果一个自动信用评分算法系统性地歧视特定种族或宗教的人，是否有任何追索权？如果你的机器学习系统的决定受到司法审查，你能向法官解释该算法是如何做出决定的吗？

1. Bryce Goodman and Seth Flaxman:
      “[European Union Regulations on Algorithmic Decision-Making and a ‘Right to Explanation’](https://arxiv.org/abs/1606.08813),” *arXiv:1606.08813*, August 31,
      2016.

      > 信用评级机构是收集数据以对人作出决定的一个老例子。糟糕的信用评分使生活变得困难，但至少信用评分通常是基于一个人的实际借贷历史的相关事实，而且记录中的任何错误都可以被纠正（尽管这些机构通常不会让这变得容易）。然而，基于机器学习的评分算法通常使用更广泛的输入，并且更加不透明，使得人们更难理解一个特定的决定是如何产生的，以及某人是否受到了不公平或歧视性的对待[89]。

1. “[A Review of the Data Broker Industry: Collection, Use, and Sale of Consumer Data for Marketing Purposes](http://educationnewyork.com/files/rockefeller_databroker.pdf),”
      Staff Report, *United States Senate Committee on Commerce, Science, and Transportation*, *commerce.senate.gov*, December 2013.

      > 我们还需要弄清楚如何防止数据被用来伤害人，而是实现其积极的潜力。例如，分析可以揭示人们生活中的财务和社会特征。一方面，这种力量可以用来集中援助和支持，帮助那些最需要的人。另一方面，它有时会被掠夺性企业利用，寻求识别弱势人群并向他们出售高成本贷款和无价值的大学学位等风险产品[87, 90]。

1. Olivia Solon:
      “[Facebook’s Failure: Did Fake News and Polarized Politics Get Trump Elected?](https://www.theguardian.com/technology/2016/nov/10/facebook-fake-news-election-conspiracy-theories)” *theguardian.com*, November 10,
      2016.

      > 即使是对人们的影响不那么直接深远的预测性应用，比如推荐系统，也有一些我们必须面对的困难问题。当服务变得善于预测用户想看的内容时，它们最终可能只向人们展示他们已经同意的观点，从而导致回声室，在回声室中，刻板印象、错误信息和两极分化会滋生。我们已经看到了社交媒体回声室对选举活动的影响[91]。

1. Donella H. Meadows and Diana Wright:
      *Thinking in Systems: A Primer*. Chelsea Green Publishing, 2008. ISBN: 978-1-603-58055-7

      > 我们不可能总是预测这种反馈环路何时发生。然而，通过对整个系统（不仅仅是计算机化的部分，还有与之互动的人）的思考，许多后果是可以预测的，这种方法被称为系统思考[92]。我们可以尝试了解一个数据分析系统如何对不同的行为、结构或特征做出反应。该系统是强化和放大了人们之间现有的差异（例如，使富人更富或穷人更穷），还是试图打击不公正现象？而且，即使有最好的意图，我们也必须提防意外的后果。

1. Daniel J. Bernstein:
      “[Listening to a ‘big data’/‘data science’ talk](https://twitter.com/hashbreaker/status/598076230437568512),” *twitter.com*, May 12, 2015.

1. Marc Andreessen:
      “[Why Software Is Eating the World](http://genius.com/Marc-andreessen-why-software-is-eating-the-world-annotated),” *The Wall Street Journal*, 20 August 2011.

1. J. M. Porup:
      “[‘Internet of Things’ Security Is Hilariously Broken and Getting Worse](http://arstechnica.com/security/2016/01/how-to-search-the-internet-of-things-for-photos-of-sleeping-babies/),” *arstechnica.com*, January 23, 2016.

      > 这个思想实验对于这本《设计监控密集型应用》来说是异常的论证，但我认为需要强有力的语言来强调这一点。在我们试图让软件 "吃掉世界 "的过程中[94]，我们已经建立了世界上有史以来最大的大规模监控基础设施。匆匆忙忙地走向物联网，我们正在迅速接近一个世界，在这个世界里，每个有人居住的空间都至少有一个与互联网连接的麦克风，其形式包括智能手机、智能电视、语音控制的助理设备、婴儿监视器，甚至是使用基于云的语音识别的儿童玩具。这些设备中的许多都有糟糕的安全记录[95]。

1. Bruce Schneier:
      [*Data and Goliath: The Hidden Battles to Collect Your Data and Control Your World*](https://www.schneier.com/books/data_and_goliath/).
      W. W. Norton, 2015. ISBN: 978-0-393-35217-7

      > 即使是最极权和压迫性的政权也只能梦想在每个房间里放一个麦克风，强迫每个人经常携带一个能够跟踪他们位置和行动的设备。然而，我们显然是自愿的，甚至是热情的，把自己扔进这个全面监控的世界。不同的是，这些数据是由公司而不是政府机构收集的[96]。

1. The Grugq:
      “[Nothing to Hide](https://grugq.tumblr.com/post/142799983558/nothing-to-hide),”
      *grugq.tumblr.com*, April 15, 2016.

      > 并非所有的数据收集都一定是监视，但将其视为监视可以帮助我们理解我们与数据收集者的关系。为什么我们似乎乐于接受企业的监控？也许你觉得你没有什么可隐瞒的--换句话说，你完全符合现有的权力结构，你不是一个被边缘化的少数人，你不需要担心被迫害[97]。不是每个人都这么幸运的。也可能是因为目的似乎是良性的--它不是公开的强迫和顺从，而只是更好的推荐和更个性化的营销。然而，结合上一节关于预测性分析的讨论，这种区别似乎不那么明显了。

1. Tony Beltramelli:
      “[Deep-Spying: Spying Using Smartwatch and Deep Learning](https://arxiv.org/abs/1512.05616),” Masters Thesis, IT University of Copenhagen, December 2015. Available at
      *arxiv.org/abs/1512.05616*

      > 我们已经看到汽车保险费与汽车中的跟踪设备相联系，健康保险的覆盖面也取决于人们是否佩戴了健身跟踪设备。当监控被用来确定对生活的重要方面有影响力的事情，如保险或就业，它就开始显得不那么良性。此外，数据分析可以显示出令人惊讶的侵入性：例如，智能手表或健身追踪器中的运动传感器可以被用来计算出你正在输入的内容（例如密码），而且精确度相当高[98]。而且分析的算法只会越来越好。

1. Shoshana Zuboff:
      “[Big Other: Surveillance Capitalism and the Prospects of an Information Civilization](http://papers.ssrn.com/sol3/papers.cfm?abstract_id=2594754),” *Journal of Information
      Technology*, volume 30, number 1, pages 75–89, April 2015.
      [doi:10.1057/jit.2015.5](http://dx.doi.org/10.1057/jit.2015.5)

      > 此外，数据是通过一个单向的过程从用户那里提取的，不是一个真正互惠的关系，也不是一个公平的价值交换。没有对话，没有选择让用户协商他们提供多少数据以及他们得到什么服务作为回报：服务和用户之间的关系是非常不对称和单方面的。条款是由服务设定的，而不是由用户设定的[99]。

1. Carina C. Zona:
      “[Consequences of an Insightful Algorithm](https://www.youtube.com/watch?v=YRI40A4tyWU),”
      at *GOTO Berlin*, November 2016.

1. Bruce Schneier:
      “[Data Is a Toxic Asset, So Why Not Throw It Out?](https://www.schneier.com/essays/archives/2016/03/data_is_a_toxic_asse.html),” *schneier.com*, March 1, 2016.

1. John E. Dunn:
      “[The UK’s 15 Most Infamous Data Breaches](http://www.techworld.com/security/uks-most-infamous-data-breaches-2016-3604586/),” *techworld.com*, November 18, 2016.

      > 因为这些数据是有价值的，所以很多人都想要它。公司当然想得到它--这就是为什么他们首先要收集它。但政府也想获得它：通过秘密交易、胁迫、法律强制，或者干脆偷窃[101]。当一个公司破产时，它所收集的个人数据是被出售的资产之一。此外，这些数据很难保证安全，所以漏洞经常发生，令人不安[102]。

1. Cory Scott:
      “[Data is not toxic - which implies no benefit - but rather hazardous material, where we must balance need vs. want](https://twitter.com/cory_scott/status/706586399483437056),”
      *twitter.com*, March 6, 2016.

      > 这些观察结果导致批评者说，数据不仅仅是一种资产，而是一种 "有毒资产"[101]，或者至少是 "危险材料"[103]。即使我们认为自己有能力防止数据被滥用，但每当我们收集数据时，我们都需要在利益与数据落入坏人手中的风险之间进行平衡：计算机系统可能被犯罪分子或敌对的外国情报机构破坏，数据可能被内部人员泄露，公司可能落入不认同我们价值观的无良管理层手中，或者国家可能被一个毫不犹豫地迫使我们交出数据的政权所接管。

1. Bruce Schneier:
      “[Mission Creep: When Everything Is Terrorism](https://www.schneier.com/essays/archives/2013/07/mission_creep_when_e.html),” *schneier.com*, July 16, 2013.

      > 在收集数据时，我们不仅需要考虑今天的政治环境，还需要考虑未来所有可能的政府。不能保证未来选出的每一个政府都会尊重人权和公民自由，所以 "安装有朝一日可能促进警察国家的技术是很差的公民卫生"[104]。

1. Lena Ulbricht and Maximilian von Grafenstein:
      “[Big Data: Big Power Shifts?](http://policyreview.info/articles/analysis/big-data-big-power-shifts),” *Internet Policy Review*, volume 5, number 1, March 2016.
      [doi:10.14763/2016.1.406](http://dx.doi.org/10.14763/2016.1.406)

1. Ellen P. Goodman and Julia Powles:
      “[Facebook and Google: Most Powerful and Secretive Empires We've Ever Known](https://www.theguardian.com/technology/2016/sep/28/google-facebook-powerful-secretive-empire-transparency),” *theguardian.com*, September 28,
      2016.

      > "知识就是力量"，这是一句老话。而且，"在避免自己受到审查的同时审查他人，是权力的最重要形式之一"[105]。这就是极权主义政府想要监控的原因：这使他们有能力控制人口。虽然今天的科技公司没有公开寻求政治权力，但他们所积累的数据和知识还是让他们对我们的生活拥有大量的权力，其中大部分是偷偷摸摸的，不受公众监督[106]。

1. [Directive 95/46/EC on the protection of individuals with regard to the processing of personal data and on the free movement of such data](http://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:31995L0046), Official Journal of the European Communities No. L 281/31,
      *eur-lex.europa.eu*, November 1995.

      > 数据保护法也许能够帮助维护个人的权利。例如，1995年的《欧洲数据保护指令》规定，个人数据必须 "为特定的、明确的和合法的目的而收集，并且不得以不符合这些目的的方式进一步处理"，此外，数据必须 "相对于收集目的而言是充分的、相关的、不过分的"[107]。

1. Brendan Van Alsenoy:
      “[Regulating Data Protection: The Allocation of Responsibility and Risk Among Actors Involved in Personal Data Processing](https://lirias.kuleuven.be/handle/123456789/545027),”
      Thesis, KU Leuven Centre for IT and IP Law, August 2016.

1. Michiel Rhoen:
      “[Beyond Consent: Improving Data Protection Through Consumer Protection Law](http://policyreview.info/articles/analysis/beyond-consent-improving-data-protection-through-consumer-protection-law),” *Internet Policy
      Review*, volume 5, number 1, March 2016.
      [doi:10.14763/2016.1.404](http://dx.doi.org/10.14763/2016.1.404)

      > 然而，在今天的互联网背景下，这一立法是否有效，令人怀疑[108]。这些规则直接违背了大数据的理念，即最大限度地收集数据，将其与其他数据集相结合，进行实验和探索，以产生新的见解。探索意味着将数据用于不可预见的目的，这与用户同意的 "特定和明确 "的目的相反（如果我们可以有意义地谈论同意的话[109]）。目前正在制定最新的法规[89]。

1. Jessica Leber:
      “[Your Data Footprint Is Affecting Your Life in Ways You Can’t Even Imagine](https://www.fastcoexist.com/3057514/your-data-footprint-is-affecting-your-life-in-ways-you-cant-even-imagine),” *fastcoexist.com*, March 15,
      2016.

      > 那些收集大量人的数据的公司反对监管，认为这是一种负担，阻碍了创新。在某种程度上，这种反对是合理的。例如，在分享医疗数据时，对隐私有明显的风险，但也有潜在的机会：如果数据分析能够帮助我们实现更好的诊断或找到更好的治疗方法，那么可以防止多少死亡[110]？过度的监管可能会阻止这种突破。要平衡这种潜在的机会和风险是很困难的[105]。

1. Maciej Cegłowski:
      “[Haunted by Data](http://idlewords.com/talks/haunted_by_data.htm),” *idlewords.com*,
      October 2015.

1. Sam Thielman:
      “[You Are Not What You Read: Librarians Purge User Data to Protect Privacy](https://www.theguardian.com/us-news/2016/jan/13/us-library-records-purged-data-privacy),” *theguardian.com*,
      January 13, 2016.

1. Conor Friedersdorf:
      “[Edward Snowden’s Other Motive for Leaking](http://www.theatlantic.com/politics/archive/2014/05/edward-snowdens-other-motive-for-leaking/370068/),” *theatlantic.com*, May 13, 2014.

1. Phillip Rogaway:
      “[The Moral Character of Cryptographic Work](http://web.cs.ucdavis.edu/~rogaway/papers/moral-fn.pdf),” Cryptology ePrint 2015/1162, December 2015.

      > 我们究竟如何实现这一目标是一个开放的问题。首先，我们不应该永远保留数据，而应该在不再需要的时候立即清除它[111, 112]。清除数据违背了不变性的理念（见 "不变性的限制"），但这个问题是可以解决的。我看到的一个有希望的方法是通过加密协议强制执行访问控制，而不仅仅是通过政策[113, 114]。总的来说，文化和态度的改变将是必要的。

