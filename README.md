# Spring Boot with Kafka Starter Example

Start ZooKeeper Server
- bin/zookeeper-server-start.sh config/zookeeper.properties

Start Kafka Server
- bin/kafka-server-start.sh config/server.properties

Create Kafka Topic
- bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic Kafka_Example

Consume from the Kafka Topic via Console
- bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic Kafka_Example --from-beginning

Publish message via WebService
- http://localhost:8081/kafka/publish/HelloWorld
- http://localhost:8081/kafka/publish/FirstMessage
