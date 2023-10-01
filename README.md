Apache-Kafka-Installation-Windows
Command line 

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















