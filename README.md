# pre-requisite

hbase-site.xml from hbase cluster must be copied to spark cluster

refer: https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-using-spark-query-hbase

# azure-spark-hbase-connector

This is a compiled connector for Hbase 2.1 and Spark 2.4

##### 1. on spark headnode: clone the repository
git clone https://github.com/angelawongsw/azure-spark-hbase-connector

##### 2. go into the clone directory
cd azure-spark-hbase-connector

##### 3. run this or 
spark-shell --jars shc-core-1.1.3-2.4-s_2.11.jar,/usr/hdp/current/hbase-client/lib/hbase-client.jar,/usr/current/hbase-client/lib/hbase-common.jar,/usr/hdp/current/hbase-client/lib/hbase-protocol.jar,/usr/hdp/current/hbase-client/lib/hbase-protocol-shaded.jar,/usr/hdp/current/hbase-client/lib/hbase-shaded-miscellaneous-2.2.0.jar,/usr/hdp/current/hbase-client/lib/hbase-shaded-protobuf-2.2.0.jar,/usr/hdp/current/hbase-client/lib/hbase-shaded-netty-2.2.0.jar

##### simplified version of this:
spark-shell --jars shc-core-1.1.3-2.4-s_2.11.jar,$(echo /usr/hdp/current/hbase-client/lib/hbase*.jar | tr ' ' ',')

##### 4. Spark shell connecting the hbase is up. 

Spark session available as 'spark'.

Welcome to Spark version 2.4.5.4.1.2.5

Using Scala version 2.11.12 (OpenJDK 64-Bit Server VM, Java 1.8.0_275)

Type in expressions to have them evaluated.

Type :help for more information.
