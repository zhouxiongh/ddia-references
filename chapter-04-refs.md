Designing Data-Intensive Applications
=====================================

Chapter 4 References
--------------------

1. “[Java Object Serialization Specification](http://docs.oracle.com/javase/7/docs/platform/serialization/spec/serialTOC.html),” *docs.oracle.com*, 2010.

1. “[Ruby 2.2.0 API Documentation](http://ruby-doc.org/core-2.2.0/),” *ruby-doc.org*, Dec 2014.

1. “[The Python 3.4.3 Standard Library Reference Manual](https://docs.python.org/3/library/pickle.html),” *docs.python.org*, February 2015.

1. “[EsotericSoftware/kryo](https://github.com/EsotericSoftware/kryo),”
    *github.com*, October 2014.

    > 语言特定的格式
    >
    > ……Java 有 java.io.Seriaalizable[1]，Ruby 有 Marshal[2]，Python 有 pickle[3] 等。此外，还有许多第三方库，例如用于 Java 的 Kryo[4]

1. “[CWE-502:   Deserialization of Untrusted Data](http://cwe.mitre.org/data/definitions/502.html),” Common Weakness Enumeration, *cwe.mitre.org*,
      July 30, 2014.

1. Steve Breen:
      “[What   Do WebLogic, WebSphere, JBoss, Jenkins, OpenNMS, and Your Application Have in Common? This   Vulnerability](http://foxglovesecurity.com/2015/11/06/what-do-weblogic-websphere-jboss-jenkins-opennms-and-your-application-have-in-common-this-vulnerability/),” *foxglovesecurity.com*, November 6, 2015.

1. Patrick McKenzie:
      “[What   the Rails Security Issue Means for Your Startup](http://www.kalzumeus.com/2013/01/31/what-the-rails-security-issue-means-for-your-startup/),” *kalzumeus.com*, January 31, 2013.

      > 语言特定的格式
      >
      > ……为了在相同的对象类型中恢复数据，解码过程需要能够实例化任意的类。这经常导致一些安全问题[5]：如果攻击者可以让应用程序解码任意的字节序列，那么它们可以实例化任意的类，这通常意味着，它们可以做些可怕的事情，比如远程执行任意代码[6，7]

1. Eishay Smith:
      “[jvm-serializers wiki](https://github.com/eishay/jvm-serializers/wiki),”
      *github.com*, November 2014.

      > 语言特定的格式
      >
      > ……例如，Java 的内置序列化由于其糟糕的性能和臃肿的编码而广为诟病

1. “[XML Is a Poor Copy of S-Expressions](http://c2.com/cgi/wiki?XmlIsaPoorCopyOfEssExpressions),” *c2.com* wiki.

      > JSON、XML 与二进制变体
      >
      > ……XML 经常被批评过于冗长和不必要的复杂

1. Matt Harris:
    “[Snowflake: An Update and Some Very Important Information](https://groups.google.com/forum/#!topic/twitter-development-talk/ahbvo3VTIYI),” email to *Twitter Development
    Talk* mailing list, October 19, 2010.

    > JSON、XML 与二进制变体
    >
    > ……twitter 的 API 返回的 JSON 包含两次推特 ID，一次是 JSON 数字，一次是十进制字符串，以解决 JavaScript 应用程序没有正确解析数字的问题

1. Shudi (Sandy) Gao, C. M. Sperberg-McQueen, and
     Henry S. Thompson: “[XML Schema 1.1](http://www.w3.org/XML/Schema),” W3C Recommendation,
     May 2001.

1. Francis Galiegue, Kris Zyp, and Gary Court:
     “[JSON Schema](http://json-schema.org/),” IETF Internet-Draft, February 2013.

     > JSON、XML 与二进制变体
     >
     > …… XML[11]和JSON[12]都有可选的模式支持

1. Yakov Shafranovich:
     “[RFC 4180: Common Format and MIME Type for Comma-Separated Values (CSV) Files](https://tools.ietf.org/html/rfc4180),” October 2005.

     > JSON、XML 与二进制变体
     >
     > ……CSV 没有任何模式……尽管其转义规则已经被正式指定[13]，但并不是所有的解析器都能正确地实现它们

1. “[MessagePack Specification](http://msgpack.org/),” *msgpack.org*.

      > 二进制编码
      >
      > ……采用 MessagePack 对示例4-1的 JSON 文档进行编码所得到的字节序列

1. Mark Slee, Aditya Agarwal, and Marc Kwiatkowski:
     “[Thrift: Scalable Cross-Language Services Implementation](http://thrift.apache.org/static/files/thrift-20070401.pdf),” Facebook technical report, April 2007.

1. “[Protocol Buffers Developer Guide](https://developers.google.com/protocol-buffers/docs/overview),” Google, Inc., *developers.google.com*.

1. Igor Anishchenko:
     “[Thrift vs Protocol Buffers vs Avro - Biased Comparison](http://www.slideshare.net/IgorAnishchenko/pb-vs-thrift-vs-avro),” *slideshare.net*, September 17, 2012.

     > Thrift 与 Protocol Buffers
     >
     > Apache Thrift[15] 和 Protocol Buffers[16] 是基于相同原理的两种二进制编码库。Apache Thrift 最初是在 Facebook 开发的， Protocol Buffers 最初是在 Google 开发的，并且都是在 2007~2008 年开源的

1. “[A Matrix of the Features Each Individual Language Library Supports](http://wiki.apache.org/thrift/LibraryFeatures),”
     *wiki.apache.org*.

     > Thrift 与 Protocol Buffers
     >
     > ……Thrift和 Protocol Buffers 各有对应的代码生成工具，采用和上面类似的模式定义，并生成支持多种编程语言的类

1. Martin Kleppmann:
     “[Schema Evolution in Avro, Protocol Buffers and Thrift](http://martin.kleppmann.com/2012/12/05/schema-evolution-in-avro-protocol-buffers-thrift.html),” *martin.kleppmann.com*, December 5, 2012.

     > Thrift 与 Protocol Buffers
     >
     > ……Thrift 有两种不同的二进制编码格式，分别称为 BinaryProtocol 和 CompactProtocol。先来看看BinaryProtocol，以这种格式编码示例4-1需要59字节

1. “[Apache Avro 1.7.7 Documentation](http://avro.apache.org/docs/1.7.7/),” *avro.apache.org*, July 2014.

      > Apache Avro 是另一种二进制编码格式

1. Doug Cutting, Chad Walters, Jim Kellerman, et al.:
     “[&#91;PROPOSAL&#93; New Subproject: Avro](http://mail-archives.apache.org/mod_mbox/hadoop-general/200904.mbox/%3C49D53694.1050906@apache.org%3E),” email thread on *hadoop-general* mailing list,
     *mail-archives.apache.org*, April 2009.

1. Tony Hoare:
     “[Null References: The Billion Dollar Mistake](http://www.infoq.com/presentations/Null-References-The-Billion-Dollar-Mistake-Tony-Hoare),” at *QCon London*,
     March 2009.

     > Avro
     >
     > ……某些编程语言中，null 是所有变量可以接收的默认值，但在 Avro 中并非如此……通过明确什么能为null 和什么不能为 null 可以帮助防止一些错误

1. Aditya Auradkar and Tom Quiggle:
      “[Introducing   Espresso—LinkedIn's Hot New Distributed Document Store](https://engineering.linkedin.com/espresso/introducing-espresso-linkedins-hot-new-distributed-document-store),” *engineering.linkedin.com*, January 21, 2015.

      > 那么 writer 模式又是什么？
      >
      > ……具有单独写入数据的数据库

1. Jay Kreps:
     “[Putting Apache Kafka to Use: A Practical Guide to Building a Stream Data Platform (Part 2)](http://blog.confluent.io/2015/02/25/stream-data-platform-2/),” *blog.confluent.io*,
     February 25, 2015.

     > 那么 writer 模式又是什么？
     >
     > ……在任何情况下，提供一个模式版本信息的数据库都非常有用，它可以充当一个说明文档来检查模式兼容性情况

1. Gwen Shapira:
     “[The Problem of Managing Schemas](http://radar.oreilly.com/2014/11/the-problem-of-managing-schemas.html),” *radar.oreilly.com*, November 4, 2014.

     > 动态生成的模式
     >
     > ……如果使用 Avro，可以很容易地根据关系模式生成 Avro 模式，并使用该模式对数据库内容进行编码，然后将其全部转储到 Avro 对象容器文件中

1. “[Apache Pig 0.14.0 Documentation](http://pig.apache.org/docs/r0.14.0/),” *pig.apache.org*, November 2014.

      > 代码生成和动态类型语言
      >
      > ……此属性与动态类型数据处理语言（如 Apache Pig）结合使用时特别有用

1. John Larmouth:
     [*ASN.1 Complete*](http://www.oss.com/asn1/resources/books-whitepapers-pubs/larmouth-asn1-book.pdf).
     Morgan Kaufmann, 1999. ISBN: 978-0-122-33435-1

     > 模式的优点
     >
     > ……它们与 ASN.1 有很多相似之处，ASN.1 是 1984 年首次被标准化的模式定义语言

1. Russell Housley, Warwick Ford, Tim Polk, and David Solo:
     “[RFC 2459: Internet X.509 Public Key Infrastructure: Certificate and CRL Profile](https://www.ietf.org/rfc/rfc2459.txt),” IETF Network Working Group, Standards Track,
     January 1999.

     > 模式的优点
     >
     > ……ASN.1 被用来定义各种网络协议，其二进制编码（DER）仍然被用于编码 SSL 证书

1. Lev Walkin:
     “[Question: Extensibility and Dropping Fields](http://lionet.info/asn1c/blog/2010/09/21/question-extensibility-removing-fields/),” *lionet.info*, September 21, 2010.

     > 模式的优点
     >
     > ……ASN.1 支持使用标签好的模式演化，类似于 Protocol Buffers 和 Thrift

1. Jesse James Garrett:
     “[Ajax: A New Approach to Web Applications](https://web.archive.org/web/20181231094556/https://www.adaptivepath.com/ideas/ajax-new-approach-web-applications/),” *adaptivepath.com*, February 18, 2005.

     > 基于服务的数据流：REST 和 RPC
     >
     > ……例如，在移动设备或桌面计算机上运行的本地应用程序也可以向服务器发出网络请求，并且在 Web 浏览器内运行的客户端 JavaScript 应用程序可以使用 XMLHttpRequest 成为 HTTP 客户端（该技术被称为 Ajax）

1. Sam Newman: *Building Microservices*.
     O'Reilly Media, 2015. ISBN: 978-1-491-95035-7

1. Chris Richardson:
     “[Microservices: Decomposing Applications for Deployability and Scalability](http://www.infoq.com/articles/microservices-intro),” *infoq.com*, May 25, 2014.

     > 基于服务的数据流：REST 和 RPC
     >
     > ……这种构建应用程序的方式传统上被称为面向服务的体系结构，最近则更名为微服务体系结构[31，32]

1. Pat Helland:
     “[Data on the Outside Versus Data on the Inside](http://cidrdb.org/cidr2005/papers/P12.pdf),” at *2nd Biennial Conference on Innovative Data Systems Research* (CIDR),
     January 2005.

     > 基于服务的数据流：REST 和 RPC
     >
     > ……虽然数据库支持使用第二章讨论的查询语言进行任意查询，但服务公开了特定于应用程序的 API，它只允许由服务的业务逻辑（应用程序代码）预先确定的输入和输出

1. Roy Thomas Fielding:
     “[Architectural Styles and the Design of Network-Based Software Architectures](https://www.ics.uci.edu/~fielding/pubs/dissertation/fielding_dissertation.pdf),” PhD Thesis, University of
     California, Irvine, 2000.

1. Roy Thomas Fielding:
     “[REST APIs Must Be Hypertext-Driven](http://roy.gbiv.com/untangled/2008/rest-apis-must-be-hypertext-driven),” *roy.gbiv.com*, October 20 2008.

     > 网络服务
     >
     > ……REST 不是一种协议，而是一个基于 HTTP 原则的设计理念

1. “[REST in Peace, SOAP](https://royal.pingdom.com/rest-in-peace-soap/),” *royal.pingdom.com*, October 15, 2010.

      > 网络服务
      >
      > ……与 SOAP 相比，REST 已经越来越受欢迎，至少在跨组织服务集成的背景下，并经常与微服务相关联

1. “[Web Services Standards as of Q1 2007](https://www.innoq.com/resources/ws-standards-poster/),” *innoq.com*, February 2007.

      > 网络服务
      >
      > ……相反，它带有庞大而复杂的多种相关编制（web 服务框架）和新增的各种功能

1. Pete Lacey:
     “[The S Stands for Simple](http://harmful.cat-v.org/software/xml/soap/simple),” *harmful.cat-v.org*, November 15, 2006.

     > 网络服务
     >
     > ……由于 WSDL 的设计目标不是人类可读的，而且 SOAP 消息通常过于复杂，无法手动构建，SOAP 用户严重依赖工具支持、代码生成和 IDE

1. Stefan Tilkov:
     “[Interview: Pete Lacey Criticizes Web Services](http://www.infoq.com/articles/pete-lacey-ws-criticism),” *infoq.com*, December 12, 2006.

     > 网络服务
     >
     > ……尽管 SOAP 及其各种扩展表面上是标准化的，但是不同厂商的实现之间的互操作性往往存在一些问题

1. “[OpenAPI Specification (fka Swagger RESTful API Documentation Specification) Version 2.0](http://swagger.io/specification/),”
     *swagger.io*, September 8, 2014.

     > 网络服务
     >
     > ……定义格式如 OpenAPI，也称为 Swagger，可用于描述 RESTful API 并帮助生成文档

1. Michi Henning:
     “[The Rise and Fall of CORBA](https://cacm.acm.org/magazines/2008/8/5336-the-rise-and-fall-of-corba/fulltext),”
     *Communications of the ACM*, volume 51, number 8, pages 52–57, August 2008.
     [doi:10.1145/1378704.1378718](http://dx.doi.org/10.1145/1378704.1378718)

     > RPC 的问题
     >
     > ……公共对象请求代理体系结构过于复杂，不提供向前或向后兼容性

1. Andrew D. Birrell and Bruce Jay Nelson:
     “[Implementing Remote Procedure Calls](http://www.cs.princeton.edu/courses/archive/fall03/cs518/papers/rpc.pdf),” *ACM Transactions on Computer Systems* (TOCS),
     volume 2, number 1, pages 39–59, February 1984.
     [doi:10.1145/2080.357392](http://dx.doi.org/10.1145/2080.357392)

     > RPC 的问题
     >
     > ……所有这些都是基于远程过程调用的思想，该思想自 20 世纪 70 年代以来就一致存在

1. Jim Waldo, Geoff Wyant, Ann Wollrath, and Sam Kendall:
     “[A Note on Distributed Computing](http://m.mirror.facebook.net/kde/devel/smli_tr-94-29.pdf),”
     Sun Microsystems Laboratories, Inc., Technical Report TR-94-29, November 1994.

1. Steve Vinoski:
     “[Convenience over Correctness](http://steve.vinoski.net/pdf/IEEE-Convenience_Over_Correctness.pdf),” *IEEE Internet Computing*, volume 12, number 4, pages 89–92, July 2008.
     [doi:10.1109/MIC.2008.75](http://dx.doi.org/10.1109/MIC.2008.75)

     > RPC的问题
     >
     > ……RPC 模型视图使向远程网络服务发出请求看起来与在同一进程中调用编程语言中的函数或方法相同。虽然起初看起来很方便，但这种方法在根本上是有缺陷的

1. Marius Eriksen:
     “[Your Server as a Function](http://monkey.org/~marius/funsrv.pdf),” at
     *7th Workshop on Programming Languages and Operating Systems* (PLOS), November 2013.
     [doi:10.1145/2525528.2525538](http://dx.doi.org/10.1145/2525528.2525538)

     > RPC 的发展方向
     >
     > ……Fetures 还简化了需要并行请求多项服务的情况，并将其结果合并

1. “[gRPC concepts](https://grpc.io/docs/guides/concepts/),” The Linux Foundation, *grpc.io*.

      > RPC 的发展方向
      >
      > ……gRPC 支持流，其中调用不仅包括一个请求和一个响应，还包括一段时间内一系列的请求和响应

1. Aditya Narayan and Irina Singh:
      “[Designing   and Versioning Compatible Web Services](https://web.archive.org/web/20141016000136/http://www.ibm.com/developerworks/websphere/library/techarticles/0705_narayan/0705_narayan.html),” *ibm.com*, March 28, 2007.

      > RPC 的数据编码和演化
      >
      > ……在 SOAP 中，请求和响应是用 XML 模式指定的。这些都是可以演化的，但有一些微妙的陷阱

1. Troy Hunt:
     “[Your API Versioning Is Wrong, Which Is Why I Decided to Do It 3 Different Wrong Ways](http://www.troyhunt.com/2014/02/your-api-versioning-is-wrong-which-is.html),” *troyhunt.com*,
     February 10, 2014.

     > RPC 的数据编码和演化
     >
     > ……关于 API 版本管理应该如何工作（即客户端如何指示它想要使用哪个版本的 API）没有统一的方案

1. “[API Upgrades](https://stripe.com/docs/upgrades),” Stripe, Inc., April 2015.

      > RPC 的数据编码和演化
      >
      > ……另一种选择是将客户端请求的 API 版本存储在服务器上，并允许通过单独的管理接口更新

1. Jonas Bonér:
      “[Upgrade in an   Akka Cluster](http://grokbase.com/t/gg/akka-user/138wd8j9e3/upgrade-in-an-akka-cluster),” email to *akka-user* mailing list, *grokbase.com*, August 28, 2013.

      > 分布式 Actor 框架
      >
      > ……但是，可以用类似 Protocol Buffers 的东西替代它，从而获得滚动升级的能力

1. Philip A. Bernstein, Sergey Bykov, Alan Geller, et al.:
      “[Orleans: Distributed Virtual Actors for Programmability and Scalability](https://www.microsoft.com/en-us/research/publication/orleans-distributed-virtual-actors-for-programmability-and-scalability/),” Microsoft Research
      Technical Report MSR-TR-2014-41, March 2014.

1. “[Microsoft Project   Orleans Documentation](http://dotnet.github.io/orleans/),” Microsoft Research, *dotnet.github.io*, 2015.

      > 分布式 Actor 框架
      >
      > ……要部署新版本的应用程序，需要建立一个新的集群，将流量从旧集群导入到新集群，然后关闭旧集群[51，52]

1. David Mercer, Sean Hinde, Yinso Chen, and Richard A O'Keefe:
      “[beginner:   Updating Data Structures](http://erlang.org/pipermail/erlang-questions/2007-October/030318.html),” email thread on *erlang-questions* mailing list, *erlang.com*,
      October 29, 2007.

      > 分布式 Actor 框架
      >
      > ……滚动升级在技术上是可能的，但要求仔细规划

1. Fred Hebert:
      “[Postscript: Maps](http://learnyousomeerlang.com/maps),” *learnyousomeerlang.com*,
      April 9, 2014.

      > 分布式 Actor 框架
      >
      > ……一些实验性的新型映射数据类型（2014年在 Erlang R17 中引入的类似于 JSON 的结构）可能会实模式的更改在将来变得更容易

