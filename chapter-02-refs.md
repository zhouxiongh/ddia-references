Designing Data-Intensive Applications
=====================================

Chapter 2 Data Models and Query Languages
--------------------

1. Edgar F. Codd:
    “[A Relational Model of Data for Large Shared Data Banks](https://www.seas.upenn.edu/~zives/03f/cis550/codd.pdf),” *Communications of the ACM*, volume 13, number
    6, pages 377–387, June 1970.
    [doi:10.1145/362384.362685](http://dx.doi.org/10.1145/362384.362685)

    > 关系模型与文档模型
    >
    > ……现在最著名的数据模型可能是 SQL，它基于 edgar codd 于 1970 年提出的关系模型

1. Michael Stonebraker and Joseph M. Hellerstein:
    “[What Goes Around Comes Around](http://mitpress2.mit.edu/books/chapters/0262693143chapm1.pdf),”
    in *Readings in Database Systems*, 4th edition, MIT Press, pages 2–41, 2005.
    ISBN: 978-0-262-69314-1

    > 关系模型与文档模型
    >
    > ……关系模型的每个竞争者都曾聒噪一时，可惜无一持久
    >
    > ……在 20 世纪 70 年代，这两个阵营之间的“大辩论”持续了很长时间

1. Pramod J. Sadalage and
    Martin Fowler: *NoSQL Distilled*. Addison-Wesley, August 2012. ISBN:
    978-0-321-82662-6

    > NoSQL 的诞生
    >
    > ……“NoSQL”这个名字是不恰当的，因为它其实并不代表具体的某些技术，它最初只是作为一个吸引人眼球的 twitter 标签频频出现在 2009 年的开源、分布式及非关系型数据库的见面会上

1. Eric Evans:
    “[NoSQL: What's in a Name?](https://web.archive.org/web/20190623045155/http://blog.sym-link.com/2009/10/30/nosql_whats_in_a_name.html),” *blog.sym-link.com*, October 30, 2009.

    > NoSQL 的诞生
    >
    > ……现在很多新兴的数据库总是会打上 NoSQL 的标签，而其含义也已经被逆向重新解释为“不仅仅是 SQL”

1. James Phillips:
      “[Surprises in Our NoSQL   Adoption Survey](http://blog.couchbase.com/nosql-adoption-survey-surprises),” *blog.couchbase.com*, February 8, 2012.

      > 

1. Michael Wagner:
      *SQL/XML:2006 – Evaluierung der Standardkonformität ausgewählter Datenbanksysteme*.
      Diplomica Verlag, Hamburg, 2010. ISBN: 978-3-836-64609-3

1. “[XML Data (SQL Server)](https://docs.microsoft.com/en-us/sql/relational-databases/xml/xml-data-sql-server?view=sql-server-ver15),” SQL Server documentation, *docs.microsoft.com*, 2013.

      > 对象-关系不匹配
      >
      > ……之后的 SQL 标准增加了对结构化数据和 XML 数据的支持。允许将多值数据存储在单行内，并支持在这些文档中查询和索引

1. “[PostgreSQL   9.3.1 Documentation](http://www.postgresql.org/docs/9.3/static/index.html),” The PostgreSQL Global Development Group, 2013.

      > 对象-关系不匹配
      >
      > ……一些数据库也支持 JSON 数据类型，例如 DB2、MySQL、PostgreSQL

1. “[The MongoDB 2.4 Manual](http://docs.mongodb.org/manual/),” MongoDB, Inc., 2013.

1. “[RethinkDB 1.11 Documentation](http://www.rethinkdb.com/docs/),” *rethinkdb.com*, 2013.

1. “[Apache CouchDB 1.6 Documentation](http://docs.couchdb.org/en/latest/),” *docs.couchdb.org*, 2014.

1. Lin Qiao, Kapil Surlaker, Shirshanka Das, et al.:
     “[On Brewing Fresh Espresso: LinkedIn’s Distributed Data Serving Platform](http://www.slideshare.net/amywtang/espresso-20952131),” at *ACM International Conference on Management
     of Data* (SIGMOD), June 2013.

     > 关系-数据不匹配
     >
     > ……于 XML 相比，JSON 的吸引力在于它更简单。面向文档的数据库（MongoDB、RethinkDB、CouchDB和Espresso）都支持该数据类型

1. Rick Long, Mark Harrington, Robert Hain, and Geoff Nicholls:
     [*IMS Primer*](http://www.redbooks.ibm.com/redbooks/pdfs/sg245352.pdf).
     IBM Redbook SG24-5352-00, IBM International Technical Support Organization, January 2000.

1. Stephen D. Bartlett:
     “[IBM’s IMS—Myths, Realities, and Opportunities](ftp://public.dhe.ibm.com/software/data/ims/pdf/TCG2013015LI.pdf),” The Clipper Group Navigator, TCG2013015LI, July 2013.

     > 文档数据库是否在重演历史？
     >
     > ……IBM 信息管理系统，最初是为了阿波罗太空计划的库存管理而开发的，并于 1968 年首次商业发布[13]，至今仍在维护和使用，通常运行在 IBM 大型机 OS/390

1. Sarah Mei:
     “[Why You Should Never Use MongoDB](http://www.sarahmei.com/blog/2013/11/11/why-you-should-never-use-mongodb/),”
     *sarahmei.com*, November 11, 2013.

     > 文档数据库是否在重演历史？
     >
     > ……开发人员必须决定复制（反规范化）多份数据，还是手动解析记录之间的引用。20 世纪六七十年代的这些问题与开发人员今天遇到的文档数据库的问题非常相似

1. J. S. Knowles and D. M. R. Bell:
     “The CODASYL Model,” in *Databases—Role and Structure: An Advanced Course*, edited by P. M.
     Stocker, P. M. D. Gray, and M. P. Atkinson, pages 19–56, Cambridge University Press, 1984. ISBN:
     978-0-521-25430-4

     > 网络模型
     >
     > 网络模型由一个称为数据系统语言会议的委员会进行标准化，并由多个不同的数据库厂商实施，它也被称为 CODASYL 模型

1. Charles W. Bachman:
     “[The Programmer as Navigator](http://dl.acm.org/citation.cfm?id=362534),”
     *Communications of the ACM*, volume 16, number 11, pages 653–658, November 1973.
     [doi:10.1145/355611.362534](http://dx.doi.org/10.1145/355611.362534)

     > 网络模型
     >
     > ……如果记录由多个父节点，则应用程序代码必须跟踪所有关系。甚至 CODASYL 委员会的成员也承认，这就像在一个 n 维数据空间中进行遍历

1. Joseph M. Hellerstein, Michael Stonebraker, and James Hamilton:
     “[Architecture of a Database System](http://db.cs.berkeley.edu/papers/fntdb07-architecture.pdf),”
     *Foundations and Trends in Databases*, volume 1, number 2, pages 141–259, November 2007.
     [doi:10.1561/1900000002](http://dx.doi.org/10.1561/1900000002)

     > 关系模型
     >
     > ……关系数据库的查询优化器称得上是一个复杂的怪兽，研究开发人员多年来持续投入，话费巨大

1. Sandeep Parikh and Kelly Stirman:
     “[Schema Design for Time Series Data in MongoDB](http://blog.mongodb.org/post/65517193370/schema-design-for-time-series-data-in-mongodb),” *blog.mongodb.org*, October 30, 2013.

     > 关系数据库与文档数据库现状
     >
     > ……例如，在使用文档数据库记录事件发生时间的应用分析程序中，可能永远不需要多对多关系

1. Martin Fowler:
     “[Schemaless Data Structures](http://martinfowler.com/articles/schemaless/),”
     *martinfowler.com*, January 7, 2013.

     > 文档模型中的模式灵活性
     >
     > ……文档数据库有时被称为无模式，但这具有误导性，因为读数据的代码通常采用某种结构因而存在某种隐形模式，而不是由数据库强制执行

1. Amr Awadallah:
     “[Schema-on-Read vs. Schema-on-Write](http://www.slideshare.net/awadallah/schemaonread-vs-schemaonwrite),” at *Berkeley EECS RAD Lab Retreat*, Santa Cruz, CA, May 2009.

     > 文档模型中的模式灵活性
     >
     > ……更准确的术语应该是读时模式，与写时模式相对应

1. Martin Odersky:
     “[The Trouble with Types](http://www.infoq.com/presentations/data-types-issues),”
     at *Strange Loop*, September 2013.

     > 文档模型中的模式灵活性
     >
     > ……正如静态与动态类型检查的支持者对于它们的优缺点存在很大的争议一样，数据库的模式执行也是一个有争议的话题，通常没有明确正确或错误的答案

1. Conrad Irwin:
     “[MongoDB—Confessions of a PostgreSQL Lover](https://speakerdeck.com/conradirwin/mongodb-confessions-of-a-postgresql-lover),” at *HTML5DevConf*, October 2013.

     > 文档模型中的模式灵活性
     >
     > ……例如，当前用户的全名存储在一个字段中，而现在想分别存储名字和姓氏

1. “[Percona Toolkit Documentation: pt-online-schema-change](http://www.percona.com/doc/percona-toolkit/2.2/pt-online-schema-change.html),” Percona Ireland Ltd., 2013.

1. Rany Keddo, Tobias Bielohlawek, and Tobias Schmidt:
     “[Large Hadron Migrator](https://github.com/soundcloud/lhm),” SoundCloud, 2013.

1. Shlomi Noach:
     “[gh-ost: GitHub's Online Schema Migration Tool for MySQL](http://githubengineering.com/gh-ost-github-s-online-migration-tool-for-mysql/),” *githubengineering.com*, August 1, 2016.

     > 文档模型中的模式灵活性
     >
     > MySQL 则需要注意，它执行 ALTER TABLE 时会把现在的整张表复制，因而当表很大时可能需要几分钟甚至几小时的停机时间，尽管现在有各种辅助工具可以解决这个限制[24-26]

1. James C. Corbett, Jeffrey Dean, Michael Epstein, et al.:
     “[Spanner: Google’s Globally-Distributed Database](https://research.google/pubs/pub39966/),”
     at *10th USENIX Symposium on Operating System Design and Implementation* (OSDI),
     October 2012.

     > 查询的数据局部性
     >
     > ……Google 的 Spanner 数据库在关系型数据模型中提供了相同的局部性，支持模式声明某些表的行应该在父表内交错

1. Donald K. Burleson:
     “[Reduce I/O with Oracle Cluster Tables](http://www.dba-oracle.com/oracle_tip_hash_index_cluster_table.htm),” *dba-oracle.com*.

     > 查询的数据局部性
     > ……Oracle 支持类似的操作，称为“多表索引集群表”特性

1. Fay Chang, Jeffrey Dean, Sanjay Ghemawat, et al.:
     “[Bigtable: A Distributed Storage System for Structured Data](https://research.google/pubs/pub27898/),” at *7th USENIX Symposium on Operating System Design and
     Implementation* (OSDI), November 2006.

     > 查询的数据局部性
     >
     > ……Bigtable 数据模型（用于Cassandra 和 Hbase）中的列族概念类似

1. Bobbie J. Cochrane and Kathy A. McKnight:
     “[DB2 JSON Capabilities, Part 1: Introduction to DB2 JSON](http://www.ibm.com/developerworks/data/library/techarticle/dm-1306nosqlforjson1/),” IBM developerWorks, June 20, 2013.

     > 文档数据库与关系数据库的融合
     >
     > ……MySQL 版本 5.7 以及 IBM DB2 10.5，都对 JSON 文档提供了相应支持

1. Herb Sutter:
     “[The Free Lunch Is Over: A Fundamental Turn Toward Concurrency in Software](http://www.gotw.ca/publications/concurrency-ddj.htm),” *Dr. Dobb's Journal*,
     volume 30, number 3, pages 202-210, March 2005.

     > 数据查询语言
     >
     > ……声明式语言通常适合于并行执行。现在 CPU 主要通过增加核，而不是通过比之前更高的时钟频率来提升速度。命令式由于指定了特定的执行顺序，很难在多核和多台机器上并行化

1. Joseph M. Hellerstein:
     “[The Declarative Imperative: Experiences and Conjectures in Distributed Logic](http://www.eecs.berkeley.edu/Pubs/TechRpts/2010/EECS-2010-90.pdf),” Electrical Engineering and
     Computer Sciences, University of California at Berkeley, Tech report UCB/EECS-2010-90, June
     2010.

     > 数据查询语言
     >
     > ……数据库都倾向于采用并行方式实现查询语言

1. Jeffrey Dean and Sanjay Ghemawat:
     “[MapReduce: Simplified Data Processing on Large Clusters](https://research.google/pubs/pub62/),” at *6th USENIX Symposium on Operating System Design and
     Implementation* (OSDI), December 2004.

     > MapReduce 查询
     >
     > ……MapReduce 是一种编程模型，用于在许多机器上批量处理海量数据，兴起于 Google

1. Craig Kerstiens:
     “[JavaScript in Your Postgres](https://blog.heroku.com/javascript_in_your_postgres),”
     *blog.heroku.com*, June 5, 2013.

     > MapReduce 查询
     >
     > ……能够在查询中使用 JavaScript 代码是一种高级查询特性，它也不限于 MapReduce，某些 SQL 数据库也可以扩展使用 JavaScript 函数

1. Nathan Bronson, Zach Amsden, George Cabrera, et al.:
     “[TAO: Facebook’s Distributed Data Store for the Social Graph](https://www.usenix.org/conference/atc13/technical-sessions/presentation/bronson),” at
     *USENIX Annual Technical Conference* (USENIX ATC), June 2013.

     > 图状数据模型
     >
     > ……facebook 维护了一个包含许多不同类型的顶点与边的大图：顶点包括人、地点、时间、签到和用户的评论；边表示哪些人是彼此的朋友，签到发生在哪些位置，谁评论了哪个帖子，谁参与了哪个事件等

1. “[Apache TinkerPop3.2.3 Documentation](http://tinkerpop.apache.org/docs/3.2.3/reference/),” *tinkerpop.apache.org*, October 2016.

      > 图状数据模型
      >
      > ……之外，还有像 Gremlin 这样的命令式图查询语言，以及 Pregel 这样的图处理框架

1. “[The Neo4j Manual v2.0.0](http://docs.neo4j.org/chunked/2.0.0/index.html),”
     Neo Technology, 2013.

1. Emil Eifrem:
     [Twitter correspondence](https://twitter.com/emileifrem/status/419107961512804352), January 3, 2014.

     > Cypher 查询语言
     >
     > Cypher 是一种用于属性图的声明式查询语言，最早为 Neo4j 图形数据库而创建[37]（它以电影“黑客帝国”中一个角色命名，于密码学的密码无关[38]）……

1. David Beckett and Tim Berners-Lee:
     “[Turtle – Terse RDF Triple Language](http://www.w3.org/TeamSubmission/turtle/),”
     W3C Team Submission, March 28, 2011.

     > 三元存储与 SPARQL
     >
     > ……

1. “[Datomic Development Resources](http://docs.datomic.com/),” Metadata Partners, LLC, 2013.

      > 语义网
      >
      > ……例如，Datomic 是一个三元存储，它与语义网并没有任何关系

1. W3C RDF Working Group:
     “[Resource Description Framework (RDF)](http://www.w3.org/RDF/),”
     *w3.org*, 10 February 2004.

     > 语义网
     >
     > 网站通常将信息以文字和图片方式发布给人类阅读，那为什么不把信息发布为机器可读的格式给计算机阅读呢？资源描述框架[41]就是这样一种机制，它让不同网站以一致的格式发布数据，这样来自不同网站的数据自动合并成一个数据网络，一种互联网级别包含所有数据的数据库

1. “[Apache Jena](http://jena.apache.org/),”
     Apache Software Foundation.

     > RDF 数据模型
     >
     > ……人眼更容易阅读像 Turtle/N3 这种格式，而采用 Apache Jena 等自动化工具可以快速转换不同的 RDF 格式

1. Steve Harris, Andy Seaborne, and Eric
     Prud'hommeaux: “[SPARQL 1.1 Query Language](http://www.w3.org/TR/sparql11-query/),”
     W3C Recommendation, March 2013.

     > SPARQL 查询语言
     >
     > SPARQL 是一种采用 RDF 数据模型的三元存储查询语言[43]，名字是 SPARQL Protocol 和 RDF query language 的缩写，发音为 “sparkle”

1. Todd J. Green, Shan Shan Huang, Boon Thau Loo, and Wenchao Zhou:
     “[Datalog and Recursive Query Processing](http://blogs.evergreen.edu/sosw/files/2014/04/Green-Vol5-DBS-017.pdf),” *Foundations and Trends in Databases*,
     volume 5, number 2, pages 105–195, November 2013.
     [doi:10.1561/1900000017](http://dx.doi.org/10.1561/1900000017)

1. Stefano Ceri, Georg Gottlob, and Letizia Tanca:
     “[What You Always Wanted to Know About Datalog (And Never Dared to Ask)](https://www.researchgate.net/profile/Letizia_Tanca/publication/3296132_What_you_always_wanted_to_know_about_Datalog_and_never_dared_to_ask/links/0fcfd50ca2d20473ca000000.pdf),” *IEEE
     Transactions on Knowledge and Data Engineering*, volume 1, number 1, pages 146–166, March 1989.
     [doi:10.1109/69.43410](http://dx.doi.org/10.1109/69.43410)

1. Serge Abiteboul, Richard Hull, and Victor Vianu:
     [*Foundations of Databases*](http://webdam.inria.fr/Alice/). Addison-Wesley, 1995.
     ISBN: 978-0-201-53771-0, available online at *webdam.inria.fr/Alice*

     > Datalog 基础
     >
     > ……Datalog 是比 SPARQL 或 Cypher 更为古老的语言，在20世纪80年代被学者广泛研究[44-46]。……它为以后的查询语言奠定了基础，因此它非常重要

1. Nathan Marz:
     “[Cascalog](https://github.com/nathanmarz/cascalog)," *github.com*.

     > Datalog 基础
     >
     > ……Cascalog[47]是用于查询 Hadoop 大数据集的 Datalog 实现

1. Dennis A. Benson,
      Ilene Karsch-Mizrachi, David J. Lipman, et al.:
      “[GenBank](https://academic.oup.com/nar/article/36/suppl_1/D25/2507746),”
      *Nucleic Acids Research*, volume 36, Database issue, pages D25–D30, December 2007.
      [doi:10.1093/nar/gkm929](http://dx.doi.org/10.1093/nar/gkm929)

      > 小结
      >
      > ……以上介绍的所有数据库都不适用于这种场景，这就是为什么研究人员开发了专门的基因组数据库软件，如 GenBank[48]

1. Fons Rademakers:
      “[ROOT for Big Data Analysis](https://indico.cern.ch/event/246453/contributions/1566610/attachments/423154/587535/ROOT-BigData-Analysis-London-2013.pdf),” at *Workshop on the Future of Big Data Management*,
      London, UK, June 2013.

      > 小结
      >
      > ……像大型强子对撞机这样的项目，现在可以处理数百 PB 级别的数据！在这种规模下，需要一些定制解决方案来避免硬件成本失控

