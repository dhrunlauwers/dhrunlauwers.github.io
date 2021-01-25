---
layout: post
title: Apache Derby - A quick overview
categories:
- General
feature_image: "/images/derby/banner.png"
---

This semester was randomly assigned a database technology to research and write a summary report.  In my case, it was *Apache Derby*. 

It would have been nice to get a chance to look into something a little more modern, but I'll save that for another post in the future.

<br>

# Relational Databases and Database Tools - Apache Derby

### Table of Contents
- [Introduction](#introduction)
- [History](#history)
- [Overview and features](#overview-and-features)
- [Requirements](#requirements)
- [Alternatives](#alternatives)
- [Usability assessment](#usability-assessment)
- [Target users and potential use cases](#target-users-and-potential-use-cases)
- [Conclusion](#conclusion)
- [References](#references)


## Introduction

Apache Derby is an open-source relational database written in Java.
Originally released in 1997 as proprietary software known as Cloudscape,
Apache Derby has a long history. As far as relational database systems
are concerned, Apache Derby is somewhat unique because it can be
deployed as a stand-alone database serving several clients, or embedded
as part of a Java application where the application serves as the
client. Because of this flexibility, Apache Derby is able to serve a
variety of use cases. The following report will examine Apache Derby
from several different perspectives, including the history, the most
prominent features, the most popular use cases, usability, and potential
alternatives.


## History

![](/images/derby/history3.png)

Apache Derby, as it is known today, was originally released under the
name Cloudscape by Cloudscape Inc. in 1997. [[1]](#1) Cloudscape was the
world's first Java-based relational database, and part of it's appeal
came from the fact it was written in Java and it could be embedded in
applications that could be easily deployed on any platform. In 1999,
Informix Software Inc. acquired Cloudscape Inc. and its Cloudscape
software. Subsequently in 2001, IBM acquired Informix Software Inc.
along with the Cloudscape software. IBM added compatibility with it's
IBM DB2 Universal Database family through a fully compliant SQL
application programming interface (API). [[2]](#2) In 2004, IBM contributed the
Cloudscape code to the Apache Software Foundation, which is when the
technology became open-source and received the name Apache Derby. After
2004, IBM continued supporting customers for Cloudscape for the
following three years while also contributing to Apache Derby. Since
then, the Apache Software Foundation has continued development on Apache
Derby until this very day.

## Overview and features

The following are the most prominent features of Apache Derby:

-   As a **relational** database, Apache Derby provides all the benefits users would expect from a database in this category - ACID compliance and fast response times for queries that look up small amounts of information.

-   A large part of the appeal for Derby is the ability to embed it into Java applications, so it's prudent to spend a few minutes explaining what Java is. Java is a popular, **general purpose programming language** intended to allow developers to *'code once, deploy anywhere'*. Java applications run on a virtual machine, known as the Java Virtual Machine (JVM), which can run the application regardless of the underlying computer architecture. As of November 2020, Java is the third most popular programming language according to the TIOBE index. [[3]](#3)

-   The third key feature of Derby is that it is **lightweight** and does not take up a lot of memory in the JVM, which means that there is as much memory as possible available for the actual application. Finally, it's important to understand that Derby does not have to be embedded in an application. It can also stand alone as a database server that can be accessed by multiple clients simultaneously. This flexibility opens up new and different use cases to the developer of not only Java applications, but applications written in other languages that can connect to the database server.

-   Finally, Apache Derby uses the familiar **SQL standard** for the majority of database interactions, allowing users familiar with other relational databases to easily take on the technology.

![](/images/derby/features.png)

## Requirements

Before seriously considering implementing Derby, it's important to take
a close look at the requirements from a software, hardware and human
resource perspective, as well as platform compatibility and licensing.

**Platform compatibility** - Since the database runs on the JVM, any
platform that also supports the JVM will also support Derby. This
includes Windows Client (Vista, 7, 8, 10), Windows Server (2008, 2012,
2016, 2019), Linux (Oracle, RedHat, Ubuntu) and OS X (64 bit). [[4]](#4)

**Software requirements** - Several software components need to be
deployed. First, some sort of operating system needs to be in place for
the JVM to operate on. Then, the Java Runtime Environment (JRE) will
need to be installed, which includes the JVM. Finally, the Apache Derby
application needs to be deployed as part of another Java application, or
as a standalone database server.

**Hardware** - The hardware requirements for all software components
should be considered. Requirements for operating systems can vary and
are out of the scope of this report. The Java Runtime Environment
requires 128MB of memory and 124MB of disk space. [[5]](#5) In addition to
this, the Apache Derby database engine requires approximately 5MB of
memory. [[6]](#6) Finally, the requirements for the Java application will
depend on the complexity of the application itself.

**Human resources** - A Java developer will be required to set up and
maintain the database and the host application if deployed in embedded
mode. Technically, there is no requirement for a database administrator
if the database is being administered programmatically by the
application itself.

**Licensing** - Apache Derby is distributed under the Apache License
2.0. The Apache License has no on-going costs associated with it, and it
allows developers to use the software for any purpose, including
distributing modified versions of the software, without concern for
royalties. [[7]](#7) This is a permissive license, which means that it does not
require derivative work to be distributed using the same license so long
as the unmodified parts of the code are clearly marked and kept under
the Apache license. [[8]](#8)

![](/images/derby/requirements.png)

## Alternatives

Another thing to consider before moving ahead with Apache Derby, or any
database management software, is to take a look at the competition.

**HyperSQL** - HyperSQL is another open-source relational database
written in Java that can be deployed as part of a Java application or as
a stand-alone database server. Some advantages of this technology over
Apache Derby are that the memory footprint is even smaller at
approximately 2MB [[9]](#9), and that the response times for more complex
queries. [[10]](#10) One potential disadvantage is that the number of
contributors to HyperSQL appears to be smaller than that of the Apache
Foundation, which means there may be some unforeseen bugs that could
arise.

**SQLite** - SQLite is an open-source embeddable relational database
written in C. Although it does not have the ability to run as a
standalone database server, SQLite could be considered a viable
alternative to Apache Derby. Some of the advantages of SQLite is the
fact that it is written in a lower-level language than Java and
therefore has fewer dependencies. In addition, it allows for the
application to be programmed in just about any programming language. [[11]](#11)

## Usability assessment

As far as usability is concerned, the fact that Apache Derby can be
installed and deployed on almost any platform is a big bonus. It gives
both developers and users a lot of flexibility. The trade-off is that it
comes with the additional dependency of the JVM. Although it is fast, it
is not as fast as some database engines that operate without the use of
a JVM like those written in C. Several command-line tools are provided,
which provides an interactive SQL environment, allows for schema
information to be exported, and allows for monitoring of system
performance. [[12]](#12) Using the database in embedded mode requires the
application to be written in Java, which is not the most approachable
programming language for first-time programmers. Setting up the database
as a standalone server allows applications written in other languages to
access the database, but this is not the case for embedding.

## Target users and potential use cases

![](/images/derby/use-cases.png)

The main target user for Derby are small businesses and websites. Some
reasons why these users are appropriate for Derby is that small
businesses and websites most likely do not have the budget to hire
separate resources to look after database administration. It allows
application developers and the application itself to take on the task of
administering the database. In addition, small businesses and websites
may have multiple users that need access to the database at the same
time, in which case the stand alone deployment of Apache Derby is
appropriate. Even just having a single staff member who is well versed
with this technology will open up a variety of possibilities. Finally,
small businesses interested in building and selling software can take
advantage of the permissive license to incorporate Apache Derby into
their own software and sell it to their customers without having to pay
royalties.

A secondary target user are companies or individuals looking for a
lightweight database engine for demonstrations and proof of concepts. It
will save the time of setting up an additional database server when it
is not required to persist beyond the lifetime of the demonstration or
proof of concept.



## Conclusion

Overall, Apache Derby offers many compelling features and can be used by
different audiences to serve a variety of use cases. Rather than
specializing in either embedded databases or stand alone databases,
Apache Derby offers substantial flexibility in terms of deployment modes
and available platforms. That being said, the open-source nature does
not lend itself to large enterprise use cases where support with high
service levels is a requirement. In addition, developers are quite
restricted in their choice of programming language when building
applications with embedded databases. Nevertheless, Apache Derby remains
a viable alternative given that it is applied in the appropriate
setting.

## References

1. <a id='1'></a> Apache Derby. (n. d.). *Wikipedia*. Retrieved from: [[https://en.wikipedia.org/wiki/Apache\_Derby](https://en.wikipedia.org/wiki/Apache_Derby)]

2.  <a id='2'></a> Paul C. Zikopoulos, George Baklarz, Dan Scott. Apache Derby \-- Off to the Races: Includes Details of IBM Cloudscape. IBM Press, 2005.

3.  <a id='3'></a>TIOBE Software BV. (2020). *TIOBE Index.* \[Fact sheet\]. Retrieved from: [[https://www.tiobe.com/tiobe-index/](https://www.tiobe.com/tiobe-index/)]

4.  <a id='4'></a>Oracle Inc. (2020). *Java Runtime Environment Requirements.* \[Fact sheet\]. Retrieved from: [[https://www.java.com/en/download/help/sysreq.html](https://www.java.com/en/download/help/sysreq.html)]

5.  <a id='5'></a>Ibid.

6.  <a id='6'></a>Apache Software Foundation. (2020). *Apache Derby.* \[Fact sheet\]. Retrieved from: [[https://db.apache.org/derby/index.html](https://db.apache.org/derby/index.html)]

7.  <a id='7'></a>Apache License. (n. d.). *Wikipedia.* Retrieved from: [[https://en.wikipedia.org/wiki/Apache\_License](https://en.wikipedia.org/wiki/Apache_License)]

8.  <a id='8'></a>Free software license. (n. d.). *Wikipedia.* Retrieved from: [[https://en.wikipedia.org/wiki/Free-software\_license](https://en.wikipedia.org/wiki/Free-software_license)]

9.  <a id='9'></a>The HSQL Development Group. (2020). *HyperSQL Database Engine*.\[Fact Sheet\]. Retrieved from: [[http://hsqldb.org](http://hsqldb.org)]

10. <a id='10'></a>The HSQL Development Group. (2020). *PolePosition performance comparison (Page 4).* \[Fact Sheet\]. Retrieved from: [[http://hsqldb.org/PolePosition.pdf](http://hsqldb.org/PolePosition.pdf)]

11. <a id='11'></a>Hipp, R. D. (2020). *SQLite Official*. \[Fact Sheet\]. Retrieved from: [[www.sqlite.org](https://www.sqlite.org/)]

12. <a id='12'></a>Ellis, S. (2016, July 1). Getting started with Apache Derby (Java DB) \[Blog Post\]. Retrieved from: [[https://www.stuartellis.name/articles/derby-javadb/](https://www.stuartellis.name/articles/derby-javadb/)]

