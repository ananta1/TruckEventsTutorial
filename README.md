# TruckEventsTutorial

This project is taken from a series of Hortonworks Tutorials that use Storm and Kafka to process real-time streaming data. The data represents a trucking fleet with smart sensors onboard. The metrics are sent in real-time over some network (satelite, LTE, radio), to an aggregation point where a cluster of Kafka brokers is running. After Kafka stores the message, a Storm Spout is used to consume the message, where it gets emitted to a stream in the Storm topology. A series of Storm bolts operate on the tuples, either evaluting the message for possible alerting, writing them to HDFS, storing in Hbase, or stored in a Hive table.

This project has a modified pom file (pom.xml) from the original, enabling it to be run on Hortonworks Sandbox, version 2.2.4. 

Here are the links to the original Hortonworks Tutorials:

http://hortonworks.com/hadoop-tutorial/simulating-transporting-realtime-events-stream-apache-kafka/

http://hortonworks.com/hadoop-tutorial/ingesting-processing-real-time-events-apache-storm/

http://hortonworks.com/hadoop-tutorial/real-time-data-ingestion-hbase-hive-using-storm-bolt/
