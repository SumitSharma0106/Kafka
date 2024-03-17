# Kafka
Understand Kafka with Spring boot on windows

Kafka is distributed system to handle the million of transactions.

Kafka works as a cluster. It consists of a broker, or server, that acts as an intermediate between the application that generates messages and the application that consumes them.

It consists of Topics, which are also known as categories, in which the generating application publishes the message, which might be String/Json/etc., and partitions to process the messages in the Topics. Topics should have distinct names.

**Kafka Producer** : Application that send the message
**Kafka Consumer** : Application that consume the message

**ZooKeeper** is a critical role in a Kafka cluster by providing distributed coordination and synchronization services

How to setup Kafka in windows:
Navigate the offical website of Kakfa : https://kafka.apache.org/quickstart
1. GET KAFKA(post downloading the Kafka, extract it, rename it as a Kafka only and post that place it in a C directory.
2. Start the ZooKeeper service: Navigate to bin/windows folder in Kakfa folder and run the below command in CMD:
zookeeper-server-start.bat ..\..\config\zookeeper.properties
3. Start the Kafka service: Navigate to bin/windows folder in Kakfa directory and run the below command in CMD:
kafka-server-start.bat ..\..\config\server.properties
4. Start the Kafka Topic: Navigate to bin/windows folder in Kakfa directory and run the below command in CMD:
kafka-topics.bat --create --topic topic-example --bootstrap-server localhost:9092


How to process message in Kafka Producer:
1. Navigate to bin/windows folder in Kakfa directory and run the below command in CMD, it will provide a console to type as message:
kafka-console-producer.bat --topic topic-example --bootstrap-server localhost:9092
> Hello World


How to consumer message in Kafka Consumer:
1. Navigate to bin/windows folder in Kakfa directory and run the below command in CMD, it will provide you all the messages are there in consumer:
kafka-console-consumer.bat --topic topic-example --from-beginning --bootstrap-server localhost:9092
> Hello World
