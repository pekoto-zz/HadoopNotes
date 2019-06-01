# Hadoop Notes
Notes and samples for Hadoop

## 1. Ecosystem

### 1.1 Core Ecosystem

* __HDFS__ (Hadoop Distributed File System): Hadoop version of GFS. Lets big data be stored across cluster of computers. All of the hard drives look like one big file system. Also maintains backup copies of data.
* __YARN__ (Yet Another Resource Negotiator): Data processing part of Hadoop. Manages resources on computing cluster. Decides which nodes are available for work, etc.
* __MapReduce__: It's MapReduce :) Consists of mappers (transform data in paralled across cluster) and reducers (put data back together)

* __PIG__: Lets you write SQL-like queries instead of having to write Java, Python, etc. The script will go through YARN and HDFS to get the data.
* __HIVE__: Similar to PIG. Makes data sitting on distributed system look like a SQL database.

* __Apache Ambari__: Sits on top of the whole system and gives an overview. Which machines are being used, execute PIG queries, etc.

* __Mesos__: Alternative to YARN.

* __Spark__: Sits on top of YARN or Mesos (at same level as MapReduce). Lets you run queries on your data.
* __Tez__: Similar to Spark. Uses a DAG to produce more optimal plans for executing queries.

* __Apache Hbase__: Exposes data to transactional platforms (other systems). Columnar data store, NoSQL database.

* __Apache Storm__: For processing streaming data quickly, in real-time.

* __Oozie__: Schedules jobs on the cluster.

* __Zookeeper__: Coordinates everything on the cluster (which nodes are up, down, etc.). Other apps rely on Zookeeper to keep track of who is master node, who's up, down, etc.

* __Scoop, Flume, Kafka__: Get data into the cluster (data ingestion). Scoop can take data from relational databases. Flume transports web logs to cluster. Kafka can collect data of any sort from a cluster of PCs and ingest it into the cluster.

 ### 1.1 External Data Storage
 
 * __MySQL__
 
 * __Cassandra__: Columnar data store
 
 * __MongoDB__: Columnar data store
 
 (Hbase could also belong here, though it is part of the Hadoop stack itself.)
 
 ### 1.2 Query Engines
 
 Lets you query data.
 
 * __Apache Drill__: Write SQL queries to query across a variety of NoSQL databases.
 
 * __Apache Phoenix__: Similar to Drill. Lets you query across data, but also gives ACID guarantees.
 
 * __Hue__: Interactively create queries.
 
 * __Presto__: Another way to execute queries across the cluster.
 
 * __Apache Zeppelin__: Takes a more notebook-like approach to querying the cluster.

(Hive could also be considered a query engine.)

