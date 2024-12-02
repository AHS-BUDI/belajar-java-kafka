## Requirement
1. [Java version 21](https://adoptium.net/)
2. [Apache Kafka 3.9.0](https://kafka.apache.org/downloads)
3. [Java Spring 3.4.0](https://start.spring.io/)

## Kafka Start
### Init Random UUID
```bash
./bin/kafka-storage.sh random-uuid
```

### Init Cluster
```bash
./bin/kafka-storage.sh format --cluster-id "random-uuid" --config config/kraft/server.properties
```
"random-uuid" from the results of generating Random UUID

### Start Kafka Service
```bash
./bin/kafka-server-start.sh config/kraft/server.properties
```

## Create Topic
Topic with partition
```bash
./bin/kafka-topics.sh --bootstrap-server localhost:9092 --create --topic helloworld --partitions 2
```

## Run Consumer
Running ConsumerApp.java

## Run Producer
Running ProducerApp.java
