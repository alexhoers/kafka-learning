# Topics

## List topics

List all Kafka topics

> docker exec -t broker kafka-topics --list --bootstrap-server broker:9092

## Create a topic 

Create a kafka topic with 3 partitions

> docker exec -t broker kafka-topics --create --topic test-topic --partitions 3 --bootstrap-server broker:9092

## Delete topic

Delete topic labelled "test-topic"

> docker exec -t broker kafka-topics --delete --topic test-topic --bootstrap-server broker:9092

## Describe topic

> docker exec -t broker kafka-topics --describe --topic test-topic --bootstrap-server broker:9092

# Producers

## Create producer

> docker exec -t broker kafka-console-producer --bootstrap-server broker:9092 --topic test-topic --property "parse.key=true" --property "key.separator=:"

# Consumers

From beginning

> docker exec -t broker kafka-console-consumer --bootstrap-server broker:9092 --topic test-topic --from-beginning --property "print.key=true" 