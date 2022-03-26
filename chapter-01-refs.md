Designing Data-Intensive Applications
=====================================

Chapter 1 References
--------------------

1.  Michael Stonebraker and Uğur Çetintemel:
    “['One Size Fits All': An Idea Whose Time Has Come and Gone](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.68.9136&rep=rep1&type=pdf),” at *21st International Conference
    on Data Engineering* (ICDE), April 2005.
    > 它们针对不同的应用场景进行优化，不适合再归为传统类型

1.  Walter L. Heimerdinger and Charles B. Weinstock:
    “[A Conceptual Framework for System Fault Tolerance](https://resources.sei.cmu.edu/asset_files/TechnicalReport/1992_005_001_16112.pdf),” Technical Report CMU/SEI-92-TR-033, Software Engineering Institute, Carnegie
    Mellon University, October 1992.
    > 注意，故障与“失效”不完全一致

1.  Ding Yuan, Yu Luo, Xin Zhuang, et al.:
    “[Simple Testing Can Prevent Most Critical Failures: An Analysis of Production Failures in Distributed Data-Intensive Systems](https://www.usenix.org/system/files/conference/osdi14/osdi14-paper-yuan.pdf),” at *11th USENIX Symposium on Operating Systems Design
    and Implementation* (OSDI), October 2014.
    > 很多关键的 bug 实际上正是由于错误处理不当导致的

1.  Yury Izrailevsky and Ariel Tseitlin:
    “[The Netflix Simian Army](https://netflixtechblog.com/the-netflix-simian-army-16e57fbab116),”
    *netflixtechblog.com*, July 19, 2011.
    > 通过故意引发故障的方式，来持续检验、测试系统的容错机制，增加对真实故障时应对的信心

1.  Daniel Ford, François Labelle, Florentina I. Popovici, et al.:
    “[Availability in Globally Distributed Storage Systems](http://research.google.com/pubs/archive/36737.pdf),”
    at *9th USENIX Symposium on Operating Systems Design and Implementation* (OSDI),
    October 2010.

1.  Brian Beach:
    “[Hard Drive Reliability Update – Sep 2014](https://www.backblaze.com/blog/hard-drive-reliability-update-september-2014/),” *backblaze.com*, September 23, 2014.
    > 研究证明硬盘的平均无故障时间（MTTF）约为 10~50 年

1.  Laurie Voss:
    “[AWS: The Good, the Bad and the Ugly](https://web.archive.org/web/20160429075023/http://blog.awe.sm/2012/12/18/aws-the-good-the-bad-and-the-ugly/),” *blog.awe.sm*, December 18, 2012.
    > 虚拟机实例经常会在事先无告警的情况下出现无法访问问题

1.  Haryadi S. Gunawi, Mingzhe Hao, Tanakorn
    Leesatapornwongsa, et al.: “[What Bugs Live in the Cloud?](http://ucare.cs.uchicago.edu/pdf/socc14-cbs.pdf),” at *5th ACM Symposium on Cloud Computing* (SoCC), November 2014.
    [doi:10.1145/2670979.2670986](http://dx.doi.org/10.1145/2670979.2670986)
    > 另一类故障是系统内的软件问题

1.  Nelson Minar:
      “[Leap Second Crashes Half   the Internet](http://www.somebits.com/weblog/tech/bad/leap-second-2012.html),” *somebits.com*, July 3, 2012.
      > 2012年6约30日发生闰秒，由于 Linux 内核中的一个 bug，导致了很多应用在该时刻发生挂起

1.  Amazon Web Services:
      “[Summary of the Amazon EC2 and Amazon RDS Service   Disruption in the US East Region](http://aws.amazon.com/message/65648/),” *aws.amazon.com*, April 29, 2011.
      > 级联故障，其中某个组件的小故障触发另一个组件故障，进而引发更多的问题

1.  Richard I. Cook:
    “[How Complex Systems Fail](http://web.mit.edu/2.75/resources/random/How%20Complex%20Systems%20Fail.pdf),” Cognitive Technologies Laboratory, April 2000.
    > 导致软件故障的 bug 通常会长时间处于引而不发的状态，直到碰到特定的触发条件。这意味着系统软件其实对使用环境存在某种假设，而这种假设多数情况都可以满足，但是在特定情况下，假设条件变得不再成立

1.  Jay Kreps:
    “[Getting Real About Distributed System Reliability](http://blog.empathybox.com/post/19574936361/getting-real-about-distributed-system-reliability),” *blog.empathybox.com*, March 19, 2012.
    > 如果系统提供某些保证，例如，在消息队列中，输出消息的数量应等于输入消息的数量，则可以不断地检查确认，如果发现差异则立即告警

1.  David Oppenheimer, Archana Ganapathi, and David A. Patterson:
    “[Why Do Internet Services Fail, and What Can Be Done About It?](http://static.usenix.org/legacy/events/usits03/tech/full_papers/oppenheimer/oppenheimer.pdf),” at *4th USENIX Symposium on
    Internet Technologies and Systems* (USITS), March 2003.
    > 例如，一项针对大型互联网服务的调查发现，运维者的配置错误居然是系统下线的首要原因，而硬件问题（服务器或网络）仅在 10%~25% 的故障中有所影响

1.  Nathan Marz:
      “[Principles   of Software Engineering, Part 1](http://nathanmarz.com/blog/principles-of-software-engineering-part-1.html),” *nathanmarz.com*, April 2, 2013.
      > 在其他行业成为遥测，一旦火箭离开地面，遥测对于跟踪和了解故障至关重要

1.  Michael Jurewitz:
    “[The Human Impact of Bugs](http://jury.me/blog/2013/3/14/the-human-impact-of-bugs),”
    *jury.me*, March 15, 2013.
    > 例如一对父母，将其所有的照片以及他们孩子的视频存放在你的照片应用中

1.  Raffi Krikorian:
    “[Timelines at Scale](http://www.infoq.com/presentations/Twitter-Timeline-Scalability),”
    at *QCon San Francisco*, November 2012.

1.  Martin Fowler:
    *Patterns of Enterprise Application Architecture*. Addison Wesley, 2002.
    ISBN: 978-0-321-12742-6

1.  Kelly Sommers:
    “[After all that run around, what caused 500ms disk latency even when we replaced physical server?](https://twitter.com/kellabyte/status/532930540777635840)” *twitter.com*, November 13, 2014.

1.  Giuseppe DeCandia, Deniz Hastorun, Madan Jampani, et al.:
    “[Dynamo: Amazon's Highly Available Key-Value Store](http://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf),” at *21st ACM Symposium on Operating
    Systems Principles* (SOSP), October 2007.

1.  Greg Linden:
    “[Make Data Useful](http://glinden.blogspot.co.uk/2006/12/slides-from-my-talk-at-stanford.html),” slides from presentation at Stanford University Data Mining class (CS345), December 2006.

1.  Tammy Everts:
    “[The Real Cost of Slow Time vs Downtime](https://www.slideshare.net/Radware/radware-cmg2014-tammyevertsslowtimevsdowntime),” *slideshare.net*, November 5, 2014.

1.  Jake Brutlag:
    “[Speed Matters](https://ai.googleblog.com/2009/06/speed-matters.html),” *ai.googleblog.com*, June 23, 2009.

1.  Tyler Treat:
    “[Everything You Know About Latency Is Wrong](http://bravenewgeek.com/everything-you-know-about-latency-is-wrong/),” *bravenewgeek.com*, December 12, 2015.

1.  Jeffrey Dean and Luiz André Barroso:
    “[The Tail at Scale](http://cacm.acm.org/magazines/2013/2/160173-the-tail-at-scale/fulltext),”
    *Communications of the ACM*, volume 56, number 2, pages 74–80, February 2013.
    [doi:10.1145/2408776.2408794](http://dx.doi.org/10.1145/2408776.2408794)

1.  Graham Cormode, Vladislav
    Shkapenyuk, Divesh Srivastava, and Bojian Xu:
    “[Forward Decay: A Practical Time Decay Model for Streaming Systems](http://dimacs.rutgers.edu/~graham/pubs/papers/fwddecay.pdf),” at *25th IEEE International Conference on Data
    Engineering* (ICDE), March 2009.

1.  Ted Dunning and Otmar Ertl:
    “[Computing Extremely Accurate Quantiles Using t-Digests](https://github.com/tdunning/t-digest),” *github.com*, March 2014.

1.  Gil Tene:
    “[HdrHistogram](http://www.hdrhistogram.org/),” *hdrhistogram.org*.

1.  Baron Schwartz:
    “[Why Percentiles Don’t Work the Way You Think](https://orangematter.solarwinds.com/2016/11/18/why-percentiles-dont-work-the-way-you-think/),” *solarwinds.com*, November 18, 2016.

1.  James Hamilton:
    “[On Designing and Deploying Internet-Scale Services](https://www.usenix.org/legacy/events/lisa07/tech/full_papers/hamilton/hamilton.pdf),” at *21st Large Installation
    System Administration Conference* (LISA), November 2007.

1.  Brian Foote and Joseph Yoder:
    “[Big Ball of Mud](http://www.laputan.org/pub/foote/mud.pdf),” at
    *4th Conference on Pattern Languages of Programs* (PLoP),
    September 1997.

1.  Frederick P Brooks: “No Silver Bullet – Essence and
    Accident in Software Engineering,” in *The Mythical Man-Month*, Anniversary
    edition, Addison-Wesley, 1995. ISBN: 978-0-201-83595-3

1.  Ben Moseley and Peter Marks:
    “[Out of the Tar Pit](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.93.8928),”
    at *BCS Software Practice Advancement* (SPA), 2006.

1.  Rich Hickey:
    “[Simple Made Easy](http://www.infoq.com/presentations/Simple-Made-Easy),”
    at *Strange Loop*, September 2011.

1.  Hongyu Pei Breivold, Ivica Crnkovic, and Peter J. Eriksson:
    “[Analyzing Software Evolvability](http://www.es.mdh.se/pdf_publications/1251.pdf),”
    at *32nd Annual IEEE International Computer Software and Applications Conference*
    (COMPSAC), July 2008.
    [doi:10.1109/COMPSAC.2008.50](http://dx.doi.org/10.1109/COMPSAC.2008.50)

