---
layout: post
title: "Apache Hadoop: an introduction and a Cheat Sheet"
description: "A brief introduction about Apache Hadoop and a useful PDF Cheat Sheet"
thumbnail: "http://oldsite.andreafortuna.org/technology/images/hadooplogo.jpg"
keywords: Programming, Apache, Hadoop, Java
category: Programming
tags: 
- Programming
- Apache
- Hadoop
- Java


---
{% include JB/setup %}

[*Apache Hadoop*](http://hadoop.apache.org/){:target="_blank"} is an open-source software framework written in *Java* for distributed storage and distributed processing of very large data sets on computer clusters built from commodity hardware. 

![image](/technology/images/hadooplogo.jpg)

All the modules in *Hadoop* are designed with a fundamental assumption:

>"Hardware failures are common and should be automatically handled by the framework"




<hr>

The Framework
--

The base *Apache Hadoop framework* is composed of the following modules:


- *Hadoop Common*

Libraries and utilities needed by other Hadoop modules.

- *Hadoop Distributed File System (HDFS)*

Distributed file-system that stores data on commodity machines, providing very high aggregate bandwidth across the cluster.

- *Hadoop YARN* 

Resource-management platform for managing computing resources in clusters and using them for scheduling of users' applications.

- *Hadoop MapReduce*

An implementation of the *MapReduce programming model* for large scale data processing.

<hr>

Not only a framework, but an ecosystem
--

![Hadoop ecosystem](/technology/images/hadoopeco.jpg)

The term *Hadoop* has come to refer not just to the base modules above, but also to the *ecosystem*, a collection of additional software packages that can be installed on top of or alongside Hadoop, such as Apache *Pig*, Apache *Hive*, Apache *HBase*, Apache *Phoenix*, Apache *Spark*, Apache *ZooKeeper*, *Cloudera Impala*, Apache *Flume*, Apache *Sqoop*, Apache *Oozie*, Apache *Storm*.

A usefull table of entire *Hadoop ecosystem* can be read from [hadoopecosystemtable.github.io](https://hadoopecosystemtable.github.io/){:target="_blank"}.

<hr>

A most complete introduction and a useful cheatsheet
--

I found on [DZone website](https://dzone.com){:target="_blank"} a very comprehensive guide, with attached a useful cheat sheet.

The guide can be read at [this address](https://dzone.com/refcardz/getting-started-apache-hadoop){:target="_blank"}, the cheatsheet is below:


<div class="video-container">
<embed src="/technology/files/apache_hadoop.pdf" pluginspage="http://www.adobe.com/products/acrobat/readstep2.html">
</div>

<hr>

A great video introduction from Stanford University
--

<div class="video-container">
<iframe src="https://www.youtube.com/embed/d2xeNpfzsYI" frameborder="0" allowfullscreen></iframe>
</div>

>Amr Awadallah introduces Apache Hadoop and asserts that it is the data operating system of the future. 
He explains many of the data problems faced by modern data systems while highlighting the benefits and features of Hadoop. 