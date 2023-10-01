Apache-Kafka-Installation-Windows
Command line 

![image](https://github.com/srss-pocs/Apache-Kafka-Installation-Windows/assets/145287517/dd006a78-05f2-485d-bad4-4a62b1a4945e)

 Producer – A Kafka producer is an application that sends data/events to a Kafka topic. Producers send the messages to the broker, which then distributes the data across the available partitions.

 Consumer – A program that subscribes to one or more topics and receives messages from brokers.

 Topics – A category or feed name to which messages are published. It represents a particular stream of data.

 Partitions – Partitions are where the messages live inside the topic. Each topic is created with one or more partitions. The partitions have a significant effect on scalable message consumption. Each partition is hosted on a separate Kafka broker.

 Broker – A single Kafka server instance that stores and manages the partitions. Brokers act as a bridge between consumers and producers.

 Leader: Each partition has one broker acting as the leader, responsible for handling all read and write requests for that partition. The leader replicates data to other brokers to provide fault tolerance.

 Replication Factor – A replication factor is the number of copies of a message over multiple brokers. The value should be less than or equal to the number of brokers that we have. Replication provides high availability and fault tolerance.

 Offset: Each message within a partition is assigned a unique identifier called an offset. It represents the position of a message within a partition.

 Consumer Offset: It indicates the position of the last message consumed by a consumer from a specific partition. It helps consumers track their progress within a partition.

 Producer Acknowledgment: It is a configuration option for the level of acknowledgment required from Kafka brokers after a message is published. It can be set to ensure message durability and reliability.



1. https://kafka.apache.org/downloads - Download Kafka
2. UnZip and set Path drive:\kafka_2.13\bin\windows [Environment Variable]
3. Download Offset Explorer from https://www.kafkatool.com/
4. Start ZooKeeper > zookeeper-server-start config\zookeeper.properties
5. Start Kafka Server > kafka-server-start config\server.properties
6. Create Topic > kafka-topics --bootstrap-server localhost:9092 --create --topic test-topic-1 --partitions 3 --replication-factor 1
7. List Topics > kafka-topics --bootstrap-server localhost:9092 --list
8. Describe Topic > kafka-topics --bootstrap-server localhost:9092 --describe --topic test-topic-1
9. Start Producer > kafka-console-producer --broker-list localhost:9092 --topic test-topic-1
10. Start Consumer > kafka-console-consumer --bootstrap-server localhost:9092 --topic test-topic-1 --from-beginning
11. Publish a Message



![image](https://github.com/srss-pocs/Apache-Kafka-Installation-Windows/assets/145287517/c525ccda-b839-4006-837b-aef9da5a8bf3)

![image](https://github.com/srss-pocs/Apache-Kafka-Installation-Windows/assets/145287517/5af58e51-f8da-4b0b-8e12-6f589eb46a5b)

![image](https://github.com/srss-pocs/Apache-Kafka-Installation-Windows/assets/145287517/c224405f-03a8-4f94-9c97-ff80c099c824)

![image](https://github.com/srss-pocs/Apache-Kafka-Installation-Windows/assets/145287517/1801b9cf-0ab8-41b3-b41a-adb932baccbd)

Open Offset Explorer

![image](https://github.com/srss-pocs/Apache-Kafka-Installation-Windows/assets/145287517/f9faaff3-ef43-4795-aa83-92bfd30a77b6)















