Designing Data-Intensive Applications
=====================================

Chapter 8 The Trouble with Distributed Systems
--------------------

1. Mark Cavage:
    “[There’s Just No Getting Around It: You’re Building a Distributed System](http://queue.acm.org/detail.cfm?id=2482856),” *ACM Queue*, volume 11, number 4, pages 80-89, April 2013.
    [doi:10.1145/2466486.2482856](http://dx.doi.org/10.1145/2466486.2482856)

1. Jay Kreps:
    “[Getting Real About Distributed System Reliability](http://blog.empathybox.com/post/19574936361/getting-real-about-distributed-system-reliability),” *blog.empathybox.com*, March 19, 2012.

    > 关键在于，分布式系统与在单节点上的软件有着非常显著的区别，你会碰到五花八门、千奇百怪的问题所导致的各种故障

1. Sydney Padua: *The Thrilling Adventures of
    Lovelace and Babbage: The (Mostly) True Story of the First Computer*. Particular Books, April 2015.  ISBN: 978-0-141-98151-2

    > 这种确定-正确性的设计目标可以一直追溯到第一台数字计算机

1. Coda Hale:
    “[You Can’t Sacrifice Partition Tolerance](http://codahale.com/you-cant-sacrifice-partition-tolerance/),” *codahale.com*, October 7, 2010.

    > 正如博客[4]所描述的那样，在这样一个现实世界中，各种各样的事情都可能会出错

1. Jeff Hodges:
    “[Notes on Distributed Systems for Young Bloods](https://web.archive.org/web/20200218095605/https://www.somethingsimilar.com/2013/01/14/notes-on-distributed-systems-for-young-bloods/),” *somethingsimilar.com*, January 14, 2013.

    > 正式由于这种不确定性和部分失效大大提高了分布式系统的复杂性

1. Antonio Regalado:
      “[Who Coined   'Cloud Computing&#x2019;?](http://www.technologyreview.com/news/425970/who-coined-cloud-computing/),” *technologyreview.com*, October 31, 2011.

1. Luiz André Barroso, Jimmy Clidaras, and Urs Hölzle:
    “[The Datacenter as a Computer: An Introduction to the Design of Warehouse-Scale Machines, Second Edition](http://www.morganclaypool.com/doi/abs/10.2200/S00516ED2V01Y201306CAC024),”
    *Synthesis Lectures on Computer Architecture*, volume 8, number 3,
    Morgan & Claypool Publishers, July 2013.
    [doi:10.2200/S00516ED2V01Y201306CAC024](http://dx.doi.org/10.2200/S00516ED2V01Y201306CAC024),
    ISBN: 978-1-627-05010-4

    > 云计算和超算
    >
    > ……在一个包含成千上万个节点的系统中，我们几乎总是可以假定某些东西发生了失效

1. David Fiala, Frank Mueller, Christian Engelmann, et al.:
    “[Detection and Correction of Silent Data Corruption for Large-Scale High-Performance Computing](http://moss.csc.ncsu.edu/~mueller/ftp/pub/mueller/papers/sc12.pdf),” at
    *International Conference for High Performance Computing, Networking, Storage and
    Analysis* (SC12), November 2012.

    > 云计算和超算
    >
    > ……等故障节点修复之后，从最近的快照检查点继续执行

1. Arjun Singh, Joon Ong, Amit Agarwal, et al.:
      “[Jupiter Rising: A   Decade of Clos Topologies and Centralized Control in Google’s Datacenter Network](http://conferences.sigcomm.org/sigcomm/2015/pdf/papers/p183.pdf),” at
      *Annual Conference of the ACM Special Interest Group on Data Communication* (SIGCOMM), August 2015.
      [doi:10.1145/2785956.2787508](http://dx.doi.org/10.1145/2785956.2787508)

      > 云计算和超算
      >
      > 大型数据中心通常基于 IP 和以太网，采用 Clos 拓扑结构提供等分带宽

1. Glenn K. Lockwood:
      “[Hadoop's   Uncomfortable Fit in HPC](http://glennklockwood.blogspot.co.uk/2014/05/hadoops-uncomfortable-fit-in-hpc.html),” *glennklockwood.blogspot.co.uk*, May 16, 2014.

      > 云计算和超算
      >
      > 高性能计算则通常特定的网络拓扑结构，例如多维网格和 toruses

1. John von Neumann:
      “[Probabilistic Logics and the Synthesis of Reliable Organisms from Unreliable Components](https://ece.uwaterloo.ca/~ssundara/courses/prob_logics.pdf),” in *Automata Studies (AM-34)*,
      edited by Claude E. Shannon and John McCarthy, Princeton University Press, 1956.
      ISBN: 978-0-691-07916-5

      > 基于不可靠的组件组建可靠的系统
      >
      > ……然而，对于计算机系统来讲，事实并非如此，在低可靠部件上构建高可靠的系统一直是计算机领域的惯用手段

1. Richard W. Hamming:
      *The Art of Doing Science and Engineering*. Taylor & Francis, 1997.
      ISBN: 978-9-056-99500-3

      > 基于不可靠的组件组建可靠的系统
      >
      > ……纠错码可以在各种通信链路上准确传输数据，包括那些可能偶尔传输出错的情况，例如无线网络出现信号干扰

1. Claude E. Shannon:
      “[A Mathematical Theory of Communication](http://cs.brynmawr.edu/Courses/cs380/fall2012/shannon1948.pdf),” *The Bell System Technical Journal*, volume 27, number 3,
      pages 379–423 and 623–656, July 1948.

      > 基于不可靠的组件组建可靠的系统
      >
      > ……但如果信号被彻底干扰，就很难保证最终可以正确接受多少数据

1. Peter Bailis and Kyle Kingsbury:
      “[The Network Is Reliable](https://queue.acm.org/detail.cfm?id=2655736),”
      *ACM Queue*, volume 12, number 7, pages 48-55, July 2014.
      [doi:10.1145/2639988.2639988](http://dx.doi.org/10.1145/2639988.2639988)

      > 现实中的网络故障
      >
      > ……一些系统研究和大量的侧面证据表明，网络问题出人意料地普遍，包括那些由公司运营的数据中心

1. Joshua B. Leners, Trinabh Gupta, Marcos K. Aguilera, and Michael Walfish:
      “[Taming Uncertainty in Distributed Systems with Help from the Network](http://www.cs.nyu.edu/~mwalfish/papers/albatross-eurosys15.pdf),” at *10th European Conference on
      Computer Systems* (EuroSys), April 2015.
      [doi:10.1145/2741948.2741976](http://dx.doi.org/10.1145/2741948.2741976)

      > 现实中的网络故障
      >
      > ……一家中型数据中心完成的调查发现，每月大约有 12 次网络故障，其中有一般涉及单台机器，有一半甚至是整个机架断网

1. Phillipa Gill, Navendu Jain, and Nachiappan Nagappan:
      “[Understanding Network Failures in Data Centers: Measurement, Analysis, and Implications](http://conferences.sigcomm.org/sigcomm/2011/papers/sigcomm/p350.pdf),” at
      *ACM SIGCOMM Conference*, August 2011.
      [doi:10.1145/2018436.2018477](http://dx.doi.org/10.1145/2018436.2018477)

      > 现实中的网络故障
      >
      > ……另一项研究分析了机架式交换机，汇聚层交换机和负载均衡器等组件的故障率，结果发现增加冗余网络设备并不会像期望的那样可以显著减少故障，主要是因为无法有效防范人为错误，而后者是造成网络中断的主要原因

1. Mark Imbriaco:
      “[Downtime Last Saturday](https://github.com/blog/1364-downtime-last-saturday),”
      *github.com*, December 26, 2012.

      > 现实中的网络故障
      >
      > ……交互及软件升级可能会触发网络拓扑重新配置，在此期间数据包的延迟显著增加，甚至超过了一分钟

1. Will Oremus:
      “[The Global Internet Is Being Attacked by Sharks, Google Confirms](http://www.slate.com/blogs/future_tense/2014/08/15/shark_attacks_threaten_google_s_undersea_internet_cables_video.html),” *slate.com*, August 15,
      2014.

      > 现实中的网络故障
      >
      > ……有报道发现鲨鱼咬破了海底电缆

1. Marc A. Donges:
      “[Re: bnx2 cards Intermittantly Going Offline](http://www.spinics.net/lists/netdev/msg210485.html),” Message to Linux *netdev* mailing list, *spinics.net*, September 13, 2012.

      > 现实中的网络故障
      >
      > 其他令人惊讶的故障还包括网络接口会丢弃所有入向数据包，但可以成功发送出向数据包，原因仍然在于网络接口配置问题

1. Kyle Kingsbury:
      “[Call Me Maybe: Elasticsearch](https://aphyr.com/posts/317-call-me-maybe-elasticsearch),” *aphyr.com*, June 15, 2014.

1. Salvatore Sanfilippo:
      “[A Few Arguments About Redis Sentinel Properties and Fail Scenarios](http://antirez.com/news/80),” *antirez.com*, October 21, 2014.

      > 现实中的网络故障
      >
      > ……集群可能会死锁，即使网络恢复了也无法提供服务[20]，甚至可能误删除数据[21]

1. Bert Hubert:
      “[The   Ultimate SO_LINGER Page, or: Why Is My TCP Not Reliable](http://blog.netherlabs.nl/articles/2009/01/18/the-ultimate-so_linger-page-or-why-is-my-tcp-not-reliable),” *blog.netherlabs.nl*, January 18, 2009.

      > 检测故障
      >
      > ……但是如果节点在处理请求的过程中发生了崩溃，则很难知道该节点实际处理了多少数据

1. Nicolas Liochon:
      “[CAP:   If All You Have Is a Timeout, Everything Looks Like a Partition](http://blog.thislongrun.com/2015/05/CAP-theorem-partition-timeout-zookeeper.html),” *blog.thislongrun.com*,
      May 25, 2015.

      > 检测故障
      >
      > ……通过脚本通知其他节点，以便新节点快速接管而跳过等待超时。HBase 采用了这样的方法

1. Jerome H. Saltzer, David P. Reed, and David D. Clark:
      “[End-To-End Arguments in System Design](https://groups.csail.mit.edu/ana/Publications/PubPDFs/End-to-End%20Arguments%20in%20System%20Design.pdf),”
      *ACM Transactions on Computer Systems*, volume 2, number 4, pages 277–288, November 1984.
      [doi:10.1145/357401.357402](http://dx.doi.org/10.1145/357401.357402)

      > 检测故障
      >
      > ……如果你想知道一个请求是否执行成功，就需要应用级别的回复

1. Matthew P. Grosvenor, Malte Schwarzkopf, Ionel Gog, et al.:
      “[Queues Don’t Matter When You Can JUMP Them!](https://www.usenix.org/system/files/conference/nsdi15/nsdi15-paper-grosvenor_update.pdf),” at *12th USENIX Symposium on Networked
      Systems Design and Implementation* (NSDI), May 2015.

      > 网络拥塞与排队
      >
      > 计算机网络上数据包延的变化根源往往在于排队

1. Guohui Wang and T. S. Eugene Ng:
      “[The Impact of   Virtualization on Network Performance of Amazon EC2 Data Center](http://www.cs.rice.edu/~eugeneng/papers/INFOCOM10-ec2.pdf),” at *29th IEEE
      International Conference on Computer Communications* (INFOCOM), March 2010.
      [doi:10.1109/INFCOM.2010.5461931](http://dx.doi.org/10.1109/INFCOM.2010.5461931)

      > 网络拥塞与排队
      >
      > ……CPU 切换虚拟机，从而导致运行的操作系统暂停几十毫秒。在这段时间，客户虚拟机无法从网络中接收任何数据，入向的包会被虚拟机管理器[26]排队缓冲，进一步增加了网络延迟的不确定性

1. Van Jacobson:
      “[Congestion   Avoidance and Control](http://www.cs.usask.ca/ftp/pub/discus/seminars2002-2003/p314-jacobson.pdf),” at *ACM Symposium on Communications Architectures and
      Protocols* (SIGCOMM), August 1988.
      [doi:10.1145/52324.52356](http://dx.doi.org/10.1145/52324.52356)

      > 网络拥塞与排队
      >
      > …… TCP 执行流量控制（也称为拥塞消除，或背压）时，节点会主动限制自己的发送速率以避免加重网络链路或接收节点负载

1. Brandon Philips:
      “[etcd: Distributed Locking and Service Discovery](https://www.youtube.com/watch?v=HJIjTTHWYnE),” at *Strange Loop*, September 2014.

1. Steve Newman:
      “[A Systematic Look at EC2 I/O](https://web.archive.org/web/20141211094156/http://blog.scalyr.com/2012/10/a-systematic-look-at-ec2-io/),”
      *blog.scalyr.com*, October 16, 2012.

      > 网络拥塞与排队
      >
      > ……如果不巧旁边有个疯狂的邻居正在大量使用资源，网络延迟就会波动很大

1. Naohiro Hayashibara, Xavier Défago, Rami Yared, and
      Takuya Katayama: “[The ϕ Accrual Failure Detector](http://hdl.handle.net/10119/4784),” Japan Advanced Institute of Science and Technology, School of Information
      Science, Technical Report IS-RR-2004-010, May 2004.

1. Jeffrey Wang:
      “[Phi Accrual Failure Detector](http://ternarysearch.blogspot.co.uk/2013/08/phi-accrual-failure-detector.html),” *ternarysearch.blogspot.co.uk*, August 11, 2013.

      > 网络拥塞与排队
      >
      > ……超时设置并不是一个不变的常量，而是持续测量响应时间机器变化（抖动），然后根据最新的响应时间分布来自动调整。可以用 Phi Accrual 故障检测器[30]完成，该检测器目前已在 Akka 和 Cassandra 中使用

1. Srinivasan Keshav: *An Engineering Approach
      to Computer Networking: ATM Networks, the Internet, and the Telephone Network*.
      Addison-Wesley Professional, May 1997. ISBN: 978-0-201-63442-6

      > 同步与异步网络
      >
      > ……在整个线路上为呼叫分配一个固定的、带宽有保证通信链路，该电路一直维持到通话结束

1. Cisco, “[Integrated Services Digital Network](https://web.archive.org/web/20181229220921/http://docwiki.cisco.com/wiki/Integrated_Services_Digital_Network),” *docwiki.cisco.com*.

1. Othmar Kyas: *ATM Networks*.
      International Thomson Publishing, 1995. ISBN: 978-1-850-32128-6

      > 同步与异步网络
      >
      > ……当新的呼叫建立后，在每个帧内分配 16 bit 的空间，在通话期间，每一方都可以保证在 250 us 内完成发送一条 16 bit 的音频数据

1. “[InfiniBand FAQ](http://www.mellanox.com/related-docs/whitepapers/InfiniBandFAQ_FQ_100.pdf),” Mellanox Technologies, December 22, 2014.

1. Jose Renato Santos, Yoshio Turner, and G. (John) Janakiraman:
      “[End-to-End Congestion Control for InfiniBand](http://www.hpl.hp.com/techreports/2002/HPL-2002-359.pdf),” at *22nd Annual Joint Conference of the IEEE Computer and
      Communications Societies* (INFOCOM), April 2003. Also published by HP Laboratories Palo
      Alto, Tech Report HPL-2002-359.
      [doi:10.1109/INFCOM.2003.1208949](http://dx.doi.org/10.1109/INFCOM.2003.1208949)

      > 同步与异步网络
      >
      > ……曾经也有一些尝试建立支持电路交换和分组交换的混合网络，比如 ATM。InfiniBand 网络有一些相似之处[35]：它在链路层实现端到端的流量控制，从而减少了网络中的排队，但仍可能会由于链路拥塞而影响延迟

1. Ulrich Windl, David Dalton, Marc Martinec, and Dale R. Worley:
      “[The NTP FAQ and HOWTO](http://www.ntp.org/ntpfaq/NTP-a-faq.htm),” *ntp.org*,
      November 2006.

      > 有可能在某种程度上实现时钟同步：最常用的机制是网络时间协议（NTP），它允许根据一组服务器报告的时间调整计算机时钟。

1. John Graham-Cumming:
      “[How and why the leap second affected Cloudflare DNS](https://blog.cloudflare.com/how-and-why-the-leap-second-affected-cloudflare-dns/),” *blog.cloudflare.com*, January 1, 2017.

      > 这些跳跃，以及它们经常忽略闰秒的事实，使得时针钟不适合测量经过的时间。

1. David Holmes:
      “[Inside the Hotspot VM: Clocks, Timers and Scheduling Events – Part I – Windows](https://web.archive.org/web/20160308031939/https://blogs.oracle.com/dholmes/entry/inside_the_hotspot_vm_clocks),”
      *blogs.oracle.com*, October 2, 2006.

      > 历史上的时间时钟也有相当粗略的分辨率，例如，在旧的Windows系统上以10毫秒为单位向前移动。

1. Steve Loughran:
      “[Time on Multi-Core, Multi-Socket Servers](http://steveloughran.blogspot.co.uk/2015/09/time-on-multi-core-multi-socket-servers.html),” *steveloughran.blogspot.co.uk*, September 17, 2015.

      > 在一个有多个CPU插槽的服务器上，每个CPU可能有一个单独的计时器，它不一定与其他CPU同步。操作系统会对任何差异进行补偿，并试图向应用线程提供一个单调的时钟视图，即使它们被安排在不同的CPU上。然而，明智的做法是，对这种单调性的保证要多加注意

1. James C. Corbett, Jeffrey Dean, Michael Epstein, et al.:
      “[Spanner: Google’s Globally-Distributed   Database](https://research.google/pubs/pub39966/),” at *10th USENIX Symposium on Operating System Design and
      Implementation* (OSDI), October 2012.

      >  计算机中的石英钟不是很准确：它有漂移（运行速度比它应该的快或慢）。时钟漂移根据机器的温度而变化。谷歌假设其服务器的时钟漂移为200ppm（百万分之一）[41]，这相当于每30秒与服务器重新同步的时钟有6毫秒的漂移，或者每天重新同步一次的时钟有17秒的漂移。这种漂移限制了你能达到的最佳精度，即使一切工作正常。

1. M. Caporaloni and R. Ambrosini:
      “[How Closely Can a Personal Computer   Clock Track the UTC Timescale Via the Internet?](https://iopscience.iop.org/0143-0807/23/4/103/),” *European Journal of
      Physics*, volume 23, number 4, pages L17–L21, June 2012.
      [doi:10.1088/0143-0807/23/4/103](http://dx.doi.org/10.1088/0143-0807/23/4/103)

      > NTP同步只能和网络延迟一样好，所以当你在一个有可变数据包延迟的拥挤网络上时，其准确性是有限制的。一项实验表明，在互联网上进行同步时，可以达到35毫秒的最小误差[42]，尽管偶尔的网络延迟高峰会导致一秒钟左右的误差。根据配置的不同，大的网络延迟可能导致NTP客户端完全放弃。

1. Nelson Minar:
      “[A Survey of the NTP Network](http://alumni.media.mit.edu/~nelson/research/ntp-survey99/),”
      *alumni.media.mit.edu*, December 1999.

1. Viliam Holub:
      “[Synchronizing Clocks in a Cassandra Cluster Pt. 1 – The Problem](https://blog.rapid7.com/2014/03/14/synchronizing-clocks-in-a-cassandra-cluster-pt-1-the-problem/),” *blog.rapid7.com*, March 14, 2014.

      > 一些NTP服务器是错误的或配置错误的，报告的时间有几个小时的偏差[43, 44]。NTP客户端是相当强大的，因为它们会查询多个服务器并忽略异常值。尽管如此，把你的系统的正确性押在互联网上一个陌生人告诉你的时间上，还是有些令人担心。

1. Poul-Henning Kamp:
      “[The One-Second War (What Time Will You   Die?)](http://queue.acm.org/detail.cfm?id=1967009),” *ACM Queue*, volume 9, number 4, pages 44–48, April 2011.
      [doi:10.1145/1966989.1967009](http://dx.doi.org/10.1145/1966989.1967009)

1. Nelson Minar:
      “[Leap Second Crashes Half   the Internet](http://www.somebits.com/weblog/tech/bad/leap-second-2012.html),” *somebits.com*, July 3, 2012.

1. Christopher Pascoe:
      “[Time,   Technology and Leaping Seconds](http://googleblog.blogspot.co.uk/2011/09/time-technology-and-leaping-seconds.html),” *googleblog.blogspot.co.uk*, September 15, 2011.

1. Mingxue Zhao and Jeff Barr:
      “[Look   Before You Leap – The Coming Leap Second and AWS](https://aws.amazon.com/blogs/aws/look-before-you-leap-the-coming-leap-second-and-aws/),” *aws.amazon.com*, May 18, 2015.

1. Darryl Veitch and Kanthaiah Vijayalayan:
      “[Network Timing   and the 2015 Leap Second](http://crin.eng.uts.edu.au/~darryl/Publications/LeapSecond_camera.pdf),” at *17th International Conference on Passive and Active
      Measurement* (PAM), April 2016.
      [doi:10.1007/978-3-319-30505-9_29](http://dx.doi.org/10.1007/978-3-319-30505-9_29)

      > 闰秒会导致一分钟的长度为59秒或61秒，这在设计时没有考虑到闰秒的系统中扰乱了计时假设[45]。闰秒使许多大型系统崩溃的事实[38, 46]表明，不正确的时钟假设是多么容易潜入系统。处理闰秒的最好方法可能是让NTP服务器 "说谎"，通过在一天中逐步进行闰秒调整（这被称为涂抹）[47, 48]，尽管实际的NTP服务器行为在实践中有所不同[49]。

1. “[Timekeeping in VMware Virtual Machines](https://www.vmware.com/content/dam/digitalmarketing/vmware/en/pdf/techpaper/Timekeeping-In-VirtualMachines.pdf),”
      Information Guide, VMware, Inc., December 2011.

      >  在虚拟机中，硬件时钟被虚拟化了，这给需要精确计时的应用程序带来了额外的挑战[50]。当一个CPU核心在虚拟机之间共享时，当另一个虚拟机在运行时，每个虚拟机会暂停几十毫秒。从一个应用程序的角度来看，这种暂停表现为时钟突然向前跳动[26]。

1. “[MiFID II / MiFIR: Regulatory Technical and Implementing Standards – Annex I (Draft)](https://www.esma.europa.eu/sites/default/files/library/2015/11/2015-esma-1464_annex_i_-_draft_rts_and_its_on_mifid_ii_and_mifir.pdf),”
      European Securities and Markets Authority, Report ESMA/2015/1464, September 2015.

      > 如果你足够关心它，投入大量资源，就有可能达到非常好的时钟精度。例如，针对金融机构的MiFID II欧洲法规草案要求所有高频交易基金将其时钟同步到UTC的100微秒之内，以帮助调试市场异常现象，如 "闪电崩盘"，并帮助检测市场操纵行为[51]。

1. Luke Bigum:
      “[Solving MiFID II Clock Synchronisation With Minimum Spend (Part 1)](https://web.archive.org/web/20170704030310/https://www.lmax.com/blog/staff-blogs/2015/11/27/solving-mifid-ii-clock-synchronisation-minimum-spend-part-1/),”
      *lmax.com*, November 27, 2015.

      > 这样的精度可以通过GPS接收器、精确时间协议（PTP）[52]以及仔细的部署和监测来实现。然而，这需要大量的努力和专业知识，而且有很多方法可以使时钟同步出错。如果你的NTP守护程序配置错误，或者防火墙阻挡了NTP流量，那么由于漂移造成的时钟误差会很快变得很大。

1. Kyle Kingsbury:
      “[Call Me Maybe: Cassandra](https://aphyr.com/posts/294-call-me-maybe-cassandra/),” *aphyr.com*, September 24, 2013.

1. John Daily:
      “[Clocks Are Bad, or, Welcome to the Wonderful World of Distributed Systems](https://riak.com/clocks-are-bad-or-welcome-to-distributed-systems/),”
      *riak.com*, November 12, 2013.

      > 问题的一部分是，不正确的时钟很容易被忽视。如果一台机器的CPU有问题，或者它的网络配置错误，它很可能根本无法工作，所以它很快就会被注意到并被修复。另一方面，如果它的石英钟有问题，或者它的NTP客户端配置错误，大多数事情似乎都能正常工作，尽管它的时钟逐渐与现实越来越远。如果某些软件依赖于精确的同步时钟，其结果更可能是无声的和微妙的数据损失，而不是戏剧性的崩溃[53, 54]。

1. Kyle Kingsbury:
      “[The Trouble with   Timestamps](https://aphyr.com/posts/299-the-trouble-with-timestamps),” *aphyr.com*, October 12, 2013.

      > 数据库的写入会神秘地消失：一个时钟滞后的节点无法覆盖一个时钟快速的节点之前写入的值，直到节点之间的时钟偏移过后[54, 55]。这种情况会导致任意数量的数据被悄悄地丢弃，而不会向应用程序报告任何错误。

1. Leslie Lamport:
      “[Time, Clocks, and the Ordering of Events in a Distributed System](https://www.microsoft.com/en-us/research/publication/time-clocks-ordering-events-distributed-system/),”
      *Communications of the ACM*, volume 21, number 7, pages 558–565, July 1978.
      [doi:10.1145/359545.359563](http://dx.doi.org/10.1145/359545.359563)

      > 所谓的逻辑时钟[56, 57]，是基于递增的计数器而不是振荡的石英晶体，是对事件排序的一个更安全的选择（见 "检测并发的写入"）。逻辑时钟不测量一天中的时间或经过的秒数，只测量事件的相对顺序（一个事件是发生在另一个事件之前还是之后）。相比之下，测量实际经过的时间的日时和单调时钟，也被称为物理时钟。我们将在 "排序保证 "中进一步研究排序问题。

1. Sandeep Kulkarni, Murat Demirbas, Deepak Madeppa, et al.:
      “[Logical Physical Clocks and Consistent Snapshots in Globally Distributed Databases](http://www.cse.buffalo.edu/tech-reports/2014-04.pdf),” State University of New York at
      Buffalo, Computer Science and Engineering Technical Report 2014-04, May 2014.

      > 你可能能够以微秒甚至纳秒的分辨率读取一台机器的时间时钟。但是，即使你能得到如此精细的测量，这也不意味着该值实际上精确到了这种精度。事实上，它很可能不是--如前所述，即使你每分钟与本地网络上的NTP服务器同步，一个不精确的石英钟的漂移也可以轻松达到几毫秒。对于公共互联网上的NTP服务器，最好的精度可能是几十毫秒，而当网络拥堵时，误差可能很容易飙升到100毫秒以上[57]。

1. Justin Sheehy:
      “[There Is No Now: Problems With Simultaneity in Distributed Systems](https://queue.acm.org/detail.cfm?id=2745385),” *ACM Queue*, volume 13, number 3, pages 36–41, March 2015.
      [doi:10.1145/2733108](http://dx.doi.org/10.1145/2733108)

      > 因此，将时钟读数视为一个时间点是没有意义的，它更像是一个置信区间内的时间范围：例如，一个系统可能有95%的把握认为现在的时间是在10.3秒和10.5秒之间，但它并不知道比这更精确的时间[58]。如果我们只知道时间+/-100毫秒，那么时间戳中的微秒级数字基本上就没有意义。

1. Murat Demirbas:
      “[Spanner: Google's Globally-Distributed Database](http://muratbuffalo.blogspot.co.uk/2013/07/spanner-googles-globally-distributed_4.html),” *muratbuffalo.blogspot.co.uk*, July 4, 2013.

1. Dahlia Malkhi and Jean-Philippe Martin:
      “[Spanner's Concurrency Control](http://www.cs.cornell.edu/~ie53/publications/DC-col51-Sep13.pdf),” *ACM SIGACT News*, volume 44, number 3, pages 73–77, September 2013.
      [doi:10.1145/2527748.2527767](http://dx.doi.org/10.1145/2527748.2527767)

      > Spanner以这种方式实现了跨数据中心的快照隔离[59, 60]。它使用TrueTime API报告的时钟置信区间，并基于以下观察：如果你有两个置信区间，每个都由最早和最晚的可能时间戳组成（A = [Aearliest, Alatest] 和 B = [Bearliest, Blatest]），并且这两个区间不重叠（即Aearliest < Alatest < Bearliest < Blatest），那么B肯定发生在A之后，这是毫无疑问的。只有当这两个区间重叠时，我们才不能确定A和B的发生顺序。

1. Manuel Bravo, Nuno Diegues, Jingna Zeng, et al.:
      “[On the Use of Clocks to Enforce Consistency in the Cloud](http://sites.computer.org/debull/A15mar/p18.pdf),” *IEEE Data Engineering Bulletin*,
      volume 38, number 1, pages 18–31, March 2015.

1. Spencer Kimball:
      “[Living Without Atomic Clocks](http://www.cockroachlabs.com/blog/living-without-atomic-clocks/),” *cockroachlabs.com*, February 17, 2016.

      > 将时钟同步用于分布式事务语义是一个积极研究的领域[57, 61, 62]。这些想法很有趣，但是它们还没有在Google之外的主流数据库中实现。

1. Cary G. Gray and David R. Cheriton:
      “[Leases: An Efficient Fault-Tolerant Mechanism for Distributed File Cache Consistency](http://web.stanford.edu/class/cs240/readings/89-leases.pdf),” at
      *12th ACM Symposium on Operating Systems Principles* (SOSP), December 1989.
      [doi:10.1145/74850.74870](http://dx.doi.org/10.1145/74850.74870)

      > 一种选择是领导者从其他节点获得一个租约，这类似于一个有超时的锁[63]。在任何时候，只有一个节点可以持有租约，因此，当一个节点获得租约时，它知道自己在一定时间内是领导者，直到租约到期。为了保持领导地位，该节点必须在租约到期前定期续约。如果该节点失败了，它就停止更新租约，所以当租约到期时，另一个节点就可以接替。

1. Todd Lipcon:
      “[Avoiding Full GCs in Apache HBase with MemStore-Local Allocation Buffers: Part 1](https://web.archive.org/web/20121101040711/http://blog.cloudera.com/blog/2011/02/avoiding-full-gcs-in-hbase-with-memstore-local-allocation-buffers-part-1/),”
      *blog.cloudera.com*, February 24, 2011.

1. Martin Thompson:
      “[Java   Garbage Collection Distilled](http://mechanical-sympathy.blogspot.co.uk/2013/07/java-garbage-collection-distilled.html),” *mechanical-sympathy.blogspot.co.uk*, July 16, 2013.

1. Alexey Ragozin:
      “[How to Tame Java GC Pauses? Surviving 16GiB Heap and Greater](https://dzone.com/articles/how-tame-java-gc-pauses),”
      *dzone.com*, June 28, 2011.

      >  许多编程语言的运行系统（如Java虚拟机）有一个垃圾收集器（GC），它偶尔需要停止所有正在运行的线程。这些 "停止世界 "的GC暂停有时会持续数分钟[64]! 即使是像HotSpot JVM的CMS这样所谓的 "并发 "垃圾收集器也不能完全与应用程序代码并行运行，甚至它们也需要不时地停止世界[65]。虽然暂停通常可以通过改变分配模式或调整GC设置来减少[66]，但如果我们想提供强有力的保证，我们必须假设最坏的情况。

1. Christopher Clark, Keir Fraser, Steven Hand, et al.:
      “[Live   Migration of Virtual Machines](http://www.cl.cam.ac.uk/research/srg/netos/papers/2005-nsdi-migration.pdf),” at *2nd USENIX Symposium on Symposium on
      Networked Systems Design & Implementation* (NSDI), May 2005.

      > 在虚拟化环境中，一个虚拟机可以被暂停（暂停所有进程的执行，并将内存内容保存到磁盘）和恢复（恢复内存内容并继续执行）。这种暂停可以在进程执行的任何时候发生，并且可以持续任意长的时间。这个功能有时被用于虚拟机从一个主机到另一个主机的实时迁移，而不需要重启，在这种情况下，暂停的长度取决于进程向内存写入的速度[67]。

1. Mike Shaver:
      “[fsyncers and   Curveballs](http://shaver.off.net/diary/2008/05/25/fsyncers-and-curveballs/),” *shaver.off.net*, May 25, 2008.

1. Zhenyun Zhuang and Cuong Tran:
      “[Eliminating   Large JVM GC Pauses Caused by Background IO Traffic](https://engineering.linkedin.com/blog/2016/02/eliminating-large-jvm-gc-pauses-caused-by-background-io-traffic),” *engineering.linkedin.com*, February 10, 2016.

      >  如果应用程序执行同步磁盘访问，一个线程可能会暂停，等待一个缓慢的磁盘I/O操作完成[68]。在许多语言中，磁盘访问可能会出人意料地发生，即使代码中没有明确提到文件访问--例如，Java的类加载器会在第一次使用类文件时懒散地加载它们，这可能发生在程序执行中的任何时候。I/O暂停和GC暂停甚至可能合谋，将它们的延迟结合起来[69]。如果磁盘实际上是一个网络文件系统或网络块设备（如亚马逊的EBS），那么I/O延迟会进一步受制于网络延迟的变化[29]。

1. David Terei and Amit Levy:
      “[Blade: A Data Center Garbage Collector](http://arxiv.org/pdf/1504.02578.pdf),”
      arXiv:1504.02578, April 13, 2015.

1. Martin Maas, Tim Harris, Krste Asanović, and John Kubiatowicz:
      “[Trash Day: Coordinating Garbage Collection in Distributed Systems](https://timharris.uk/papers/2015-hotos.pdf),” at *15th USENIX Workshop on Hot Topics in Operating
      Systems* (HotOS), May 2015.

1. “[Predictable Low Latency](http://cdn2.hubspot.net/hubfs/1624455/Website_2016/content/White%20papers/Cinnober%20on%20GC%20pause%20free%20Java%20applications.pdf),” Cinnober Financial Technology AB, *cinnober.com*, November 24, 2013.

      > 一个新出现的想法是把GC暂停当作一个节点的短暂计划停顿，让其他节点在一个节点收集垃圾时处理来自客户端的请求。如果运行时可以警告应用程序，一个节点很快就需要GC暂停，那么应用程序可以停止向该节点发送新的请求，等待它完成处理未完成的请求，然后在没有请求的情况下执行GC。这个技巧对客户隐藏了GC暂停，减少了响应时间的高百分比[70, 71]。一些对延迟敏感的金融交易系统[72]使用了这种方法。

1. Martin Fowler:
      “[The LMAX Architecture](http://martinfowler.com/articles/lmax.html),”
      *martinfowler.com*, July 12, 2011.

      > 这个想法的一个变种是，只对短命的对象（收集速度快）使用垃圾收集器，并定期重启进程，在它们积累了足够多的长命对象，需要对长命对象进行全面的GC[65, 73]。一次可以重启一个节点，流量可以在计划的重启前从节点转移出去，就像在滚动升级中一样（见第四章）。

1. Flavio P. Junqueira and Benjamin Reed:
      *ZooKeeper: Distributed Process Coordination*. O'Reilly Media, 2013.
      ISBN: 978-1-449-36130-3

      > 如果ZooKeeper被用作锁服务，事务ID zxid或节点版本cversion可以被用作围栏令牌。由于它们被保证是单调增长的，所以它们具有所需的属性[74]。

1. Enis Söztutar:
      “[HBase and HDFS: Understanding Filesystem Usage in HBase](http://www.slideshare.net/enissoz/hbase-and-hdfs-understanding-filesystem-usage),” at *HBaseCon*,
      June 2013.

1. Caitie McCaffrey:
      “[Clients Are Jerks: AKA How Halo 4 DoSed the Services at Launch & How We Survived](http://caitiem.com/2015/06/23/clients-are-jerks-aka-how-halo-4-dosed-the-services-at-launch-how-we-survived/),” *caitiem.com*,
      June 23, 2015.

      > 在服务器端检查令牌似乎是一个缺点，但它可以说是一件好事：一个服务假设它的客户总是表现良好是不明智的，因为客户往往是由那些优先级与运行服务的人的优先级非常不同的人管理的[76]。因此，对于任何服务来说，保护自己免受意外的滥用客户的影响是一个好主意。

1. Leslie Lamport, Robert Shostak, and Marshall Pease:
      “[The Byzantine Generals Problem](https://www.microsoft.com/en-us/research/publication/byzantine-generals-problem/),”
      *ACM Transactions on Programming Languages and Systems* (TOPLAS), volume 4, number 3, pages 382–401, July 1982.
      [doi:10.1145/357172.357176](http://dx.doi.org/10.1145/357172.357176)

      > 如果存在节点可能 "撒谎"（发送任意的错误或损坏的响应）的风险，分布式系统问题就会变得更加困难--例如，如果一个节点可能声称收到了某个特定的消息，但实际上它并没有收到。这种行为被称为拜占庭故障，而在这种不信任的环境中达成共识的问题被称为拜占庭将军问题[77]。

1. Jim N. Gray:
      “[Notes on Data Base Operating Systems](http://jimgray.azurewebsites.net/papers/dbos.pdf),” in *Operating Systems: An Advanced Course*, Lecture
      Notes in Computer Science, volume 60, edited by R. Bayer, R. M. Graham, and G. Seegmüller,
      pages 393–481, Springer-Verlag, 1978. ISBN: 978-3-540-08755-7

      > 拜占庭将军问题是所谓的两个将军问题[78]的概括，它想象了这样一种情况：两个军队的将军需要就一个作战计划达成一致。由于他们在两个不同的地方安营扎寨，他们只能通过信使进行沟通，而信使有时会被延迟或丢失（就像网络中的数据包）。我们将在第九章讨论这个共识问题。

1. Brian Palmer:
      “[How Complicated Was the Byzantine Empire?](http://www.slate.com/articles/news_and_politics/explainer/2011/10/the_byzantine_tax_code_how_complicated_was_byzantium_anyway_.html),” *slate.com*, October 20, 2011.

1. Leslie Lamport:
      “[My Writings](http://lamport.azurewebsites.net/pubs/pubs.html),” *lamport.azurewebsites.net*, December 16, 2014.
      This page can be found by searching the web for the 23-character string obtained by removing the hyphens from the string
      `allla-mport-spubso-ntheweb`.

      > 拜占庭是一座古希腊城市，后来成为君士坦丁堡，位于现在土耳其伊斯坦布尔的地方。没有任何历史证据表明拜占庭的将军们比其他地方的将军更容易搞阴谋诡计。相反，这个名字来自于拜占庭的含义，即过分复杂、官僚、狡猾，这在计算机之前很久就被用于政治[79]。兰波特想选择一个不会冒犯任何读者的国籍，有人建议他把它叫做《阿尔巴尼亚将军问题》并不是一个好主意[80]。

1. John Rushby:
      “[Bus Architectures for   Safety-Critical Embedded Systems](http://www.csl.sri.com/papers/emsoft01/emsoft01.pdf),” at *1st International Workshop on Embedded Software*
      (EMSOFT), October 2001.

1. Jake Edge:
      “[ELC: SpaceX Lessons Learned](http://lwn.net/Articles/540368/),” *lwn.net*,
      March 6, 2013.

      > 在航空航天环境中，计算机内存或CPU寄存器中的数据可能被辐射破坏，导致它以任意不可预测的方式对其他节点作出反应。由于系统故障将是非常昂贵的（例如，飞机坠毁并杀死机上所有人，或火箭与国际空间站相撞），飞行控制系统必须容忍拜占庭故障[81, 82]。

1. Andrew Miller and Joseph J. LaViola, Jr.:
      “[Anonymous   Byzantine Consensus from Moderately-Hard Puzzles: A Model for Bitcoin](http://nakamotoinstitute.org/static/docs/anonymous-byzantine-consensus.pdf),” University of Central
      Florida, Technical Report CS-TR-14-01, April 2014.

      > 在一个有多个参与组织的系统中，一些参与者可能试图欺骗或诈骗他人。在这种情况下，一个节点简单地信任另一个节点的信息是不安全的，因为它们可能是带着恶意发送的。例如，像比特币和其他区块链这样的点对点网络可以被认为是一种让相互不信任的各方就交易是否发生达成一致的方式，而无需依赖中央机构[83]。

1. James Mickens:
      “[The Saddest Moment](https://www.usenix.org/system/files/login-logout_1305_mickens.pdf),” *USENIX ;login: logout*, May 2013.

      > 然而，在我们在本书中讨论的各类系统中，我们通常可以安全地假设不存在拜占庭故障。在你的数据中心，所有的节点都是由你的组织控制的（所以他们有可能被信任），而且辐射水平足够低，内存损坏不是一个大问题。使系统具有拜占庭式容错能力的协议相当复杂[84]，而容错的嵌入式系统依赖于来自硬件层面的支持[81]。在大多数服务器端的数据系统中，部署拜占庭容错解决方案的成本使其不切实际。

1. Evan Gilman:
      “[The   Discovery of Apache ZooKeeper’s Poison Packet](http://www.pagerduty.com/blog/the-discovery-of-apache-zookeepers-poison-packet/),” *pagerduty.com*, May 7, 2015.

1. Jonathan Stone and Craig Partridge:
      “[When   the CRC and TCP Checksum Disagree](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.27.7611&rep=rep1&type=pdf),” at *ACM Conference on Applications,
      Technologies, Architectures, and Protocols for Computer Communication* (SIGCOMM), August 2000.
      [doi:10.1145/347059.347561](http://dx.doi.org/10.1145/347059.347561)

1. Evan Jones:
      “[How Both TCP and Ethernet   Checksums Fail](http://www.evanjones.ca/tcp-and-ethernet-checksums-fail.html),” *evanjones.ca*, October 5, 2015.

      > 由于硬件问题或操作系统、驱动程序、路由器等的错误，网络数据包有时确实会被破坏。通常情况下，损坏的数据包会被TCP和UDP中内置的校验和捕获，但有时它们会逃避检测[85, 86, 87]。简单的措施通常足以防止这种损坏，如应用级协议中的校验和。

1. Cynthia Dwork, Nancy Lynch, and Larry Stockmeyer:
      “[Consensus in the   Presence of Partial Synchrony](http://www.net.t-labs.tu-berlin.de/~petr/ADC-07/papers/DLS88.pdf),” *Journal of the ACM*, volume 35, number 2, pages 288–323,
      April 1988. [doi:10.1145/42282.42283](http://dx.doi.org/10.1145/42282.42283)

      > 同步模型假设了有界的网络延迟、有界的进程暂停和有界的时钟误差。这并不意味着完全同步的时钟或零网络延迟；它只是意味着你知道网络延迟、停顿和时钟漂移永远不会超过某个固定的上限[88]。同步模型不是大多数实际系统的现实模型，因为（正如本章所讨论的）无界延迟和停顿确实会发生。

1. Peter Bailis and Ali Ghodsi:
      “[Eventual Consistency Today: Limitations, Extensions, and Beyond](http://queue.acm.org/detail.cfm?id=2462076),” *ACM Queue*, volume 11, number 3, pages 55-63, March 2013.
      [doi:10.1145/2460276.2462076](http://dx.doi.org/10.1145/2460276.2462076)

      > 这两种属性的区别是什么？一个赠品是，有效性属性在其定义中经常包括 "最终 "这个词。(是的，你猜对了--最终的一致性是一种活泼性属性[89]）。

1. Bowen Alpern and Fred B. Schneider:
      “[Defining Liveness](https://www.cs.cornell.edu/fbs/publications/DefLiveness.pdf),”
      *Information Processing Letters*, volume 21, number 4, pages 181–185, October 1985.
      [doi:10.1016/0020-0190(85)90056-0](http://dx.doi.org/10.1016/0020-0190(85)90056-0)

      > 安全性通常被非正式地定义为没有坏事发生，而有效性是指最终会有好事发生。然而，最好不要对这些非正式的定义作过多的解读，因为好和坏的含义是主观的。安全性和活泼性的实际定义是精确和数学化的[90]。

1. Flavio P. Junqueira:
      “[Dude, Where’s My Metadata?](http://fpj.me/2015/05/28/dude-wheres-my-metadata/),”
      *fpj.me*, May 28, 2015.

1. Scott Sanders:
      “[January 28th Incident Report](https://github.com/blog/2106-january-28th-incident-report),” *github.com*, February 3, 2016.

      > 例如，崩溃恢复模型中的算法通常假设稳定存储中的数据能在崩溃中存活。然而，如果磁盘上的数据被破坏了，或者由于硬件错误或错误配置，数据被抹去了，会发生什么？如果一台服务器有一个固件错误，在重启时无法识别其硬盘，即使硬盘正确地连接到服务器上，又会发生什么呢[92]？

1. Jay Kreps:
      “[A Few Notes on Kafka and Jepsen](http://blog.empathybox.com/post/62279088548/a-few-notes-on-kafka-and-jepsen),” *blog.empathybox.com*, September 25, 2013.

      > 算法的理论描述可以声明某些事情被简单地假定为不会发生--在非拜占庭系统中，我们确实必须对可能和不可能发生的故障做出一些假设。然而，真正的实现可能仍然需要包括一些代码来处理假定不可能发生的事情，即使这种处理归结为printf("Sucks to be you")和exit(666)--即让人类操作员来清理这个烂摊子[93]。(这可以说是计算机科学和软件工程之间的区别）。

1. Thanh Do, Mingzhe Hao, Tanakorn
      Leesatapornwongsa, et al.:
      “[Limplock: Understanding the Impact of Limpware on Scale-out Cloud Systems](http://ucare.cs.uchicago.edu/pdf/socc13-limplock.pdf),” at *4th ACM Symposium on Cloud Computing*
      (SoCC), October 2013.
      [doi:10.1145/2523616.2523627](http://dx.doi.org/10.1145/2523616.2523627)

      > 要容忍故障，第一步是检测它们，但即使这样也很难。大多数系统没有一个准确的机制来检测一个节点是否发生了故障，所以大多数分布式算法依靠超时来确定一个远程节点是否仍然可用。然而，超时不能区分网络和节点故障，可变的网络延迟有时会导致一个节点被错误地怀疑为崩溃。此外，有时一个节点可能处于降级状态：例如，一个千兆网络接口可能由于驱动错误而突然下降到1 Kb/s的吞吐量[94]。这样一个 "一瘸一拐 "但没有死亡的节点可能比一个干净的故障节点更难处理。

1. Frank McSherry, Michael Isard, and Derek G. Murray:
      “[Scalability! But at What COST?](http://www.frankmcsherry.org/assets/COST.pdf),”
      at *15th USENIX Workshop on Hot Topics in Operating Systems* (HotOS),
      May 2015.

      > 如果你习惯于在理想化的单台计算机的完美数学中编写软件，在那里，相同的操作总是确定性地返回相同的结果，那么，转移到分布式系统的混乱的物理现实中，可能会有点震惊。相反，如果一个问题可以在单台计算机上解决，分布式系统工程师往往会认为它是微不足道的[5]，而且现在单台计算机确实可以做很多事[95]。如果你能避免打开潘多拉的盒子，只是把东西放在一台机器上，一般来说是值得这样做的。

