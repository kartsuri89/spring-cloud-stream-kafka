# spring-cloud-stream-kafka

#Strat Zookeeper server

  zookeeper-server-start.bat D:\sandbox\kafka_2.13-3.2.0\config\zookeeper.properties

#Strat Kafka server

  kafka-server-start.bat D:\sandbox\kafka_2.13-3.2.0\config\server.properties

#Create Topic

  kafka-topics.bat --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 -topic kafka-impl

#List down all available topics

  kafka-topics.bat --list --bootstrap-server localhost:9092
  
# Delete a specific Topic

  kafka-topics.bat --delete --bootstrap-server localhost:9092 --topic kafka-impl

#Produce a message

  kafka-console-producer.bat --broker-list localhost:9092 --topic kafka-impl

#Consume a message

  kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic kafka-impl
