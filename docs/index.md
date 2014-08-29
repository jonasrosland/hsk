**THIS IS A DRAFT**

#EMC Hadoop Starter Kits

##Abstract
This white paper describes how to create a Hadoop environment utilizing Cloudera Manager and an EMC Isilon Scale-Out NAS for HDFS accessible shared storage. VMware Big Data Extensions is used to provision and manage the compute resources. 

##Introduction
IDC published an update to their Digital Universe study in December 2012 and found that the rate of digital data creation is not only continuing to grow, but the rate is actually accelerating. By the end of this decade we will create 40 Zettabytes of new digital information yearly or the equivalent of 1.7MB of digital information for every man, woman, and child every second of every day. 

This information explosion is creating new opportunities for our businesses to leverage digital information to serve their customers better, faster, and most cost effectively through Big Data Analytics applications.  Hadoop technologies can be cost effective solutions and can manage structured, semi-structured and unstructured data unlike traditional solutions such as RDBMS. The need to track and analyze consumer behavior, maintain inventory and space, target marketing offers on the basis of consumer preferences and attract and retain consumers, are some of the factors pushing the demand for Big Data Analytics solutions using Hadoop technologies. According to a new market report published by Transparency Market Research (http://www.transparencymarketresearch.com) "Hadoop Market - Global Industry Analysis, Size, Share, Growth, Trends, and Forecast, 2012- 2018," the global Hadoop market was worth USD 1.5 billion in 2012 and is expected to reach USD 20.9 billion in 2018, growing at a CAGR of 54.7% from 2012 to 2018. 

Hadoop like any new technology can be time consuming, and expensive for our customers to get deployed and operational. When we surveyed a number of our customers, two main challenges were identified to getting started: confusion over which Hadoop distribution to use and how to deploy using existing IT assets and knowledge. Hadoop software is distributed by several vendors including Pivotal, Hortonworks, and Cloudera with proprietary extensions. In addition to these distributions, Apache distributes a free open source version. From an infrastructure perspective many Hadoop deployments start outside the IT data center and do not leverage the existing IT automation, storage efficiency, and protection capabilities. Many customers cited the time it took IT to deploy Hadoop as the primary reason to start with a deployment outside of IT.

This guide is intended to simplify Hadoop deployments by creating a shared storage model with EMC Isilon scale out NAS and using the industry leader in Enterprise Hadoop, Cloudera, reduce the time to deployment, and the cost of deployment leveraging Cloudera Manager tool’s that can automate Hadoop cluster deployments.

##Audience
This white paper is intended for IT program managers, IT architects, Developers, and IT management to easily deploy Cloudera Hadoop with automation tools and leverage EMC Isilon for HDFS shared storage. It can be used by somebody who does not yet have an EMC Isilon cluster by downloading the free EMC Isilon OneFS Simulator which can be installed as a virtual machine for testing and training. However, this document can also be used by somebody who will be installing in a production environment as best-practices are followed whenever possible.

##Apache Hadoop projects
Apache Hadoop is an open source, batch data processing system for enormous amounts of data.  Hadoop runs as a platform that provides cost-effective, scalable infrastructure for building Big Data analytic applications. All Hadoop clusters contain a distributed file system called the Hadoop Distributed File System (HDFS), a computation layer called MapReduce.

The Apache Hadoop project contains the following subprojects:

- **Hadoop Distributed File System (HDFS)** – A distributed file system that provides high-throughput access to application data.
- **Hadoop MapReduce** – A software framework for writing applications to reliably process large amounts of data in parallel across a cluster.

Hadoop is supplemented by an ecosystem of Apache projects, such as Pig, Hive, Sqoop, Flume, Oozie, Whirr, HBase, and Zookeeper that extend the value of Hadoop and improves its usability.

Version 2 of Apache Hadoop introduces YARN, a sub-project of Hadoop that separates the resource management and processing components. YARN was born of a need to enable a broader array of interaction patterns for data stored in HDFS beyond MapReduce. The YARN-based architecture of Hadoop 2.0 provides a more general processing platform that is not constrained to MapReduce.

For full details of the Apache Hadoop project see [http://hadoop.apache.org/](http://hadoop.apache.org/).

