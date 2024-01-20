# kafka-learning

## Docker quickstart

Follow the guide here: https://docs.confluent.io/platform/6.2/quickstart/ce-docker-quickstart.html

Commands:

> docker-compose up -d

> docker-compose ps


# Kafka CLI

Your first step is to create a topic to produce to and consume from. Use the following command to create the topic:

> docker exec -t broker kafka-topics --create --topic orders-avro --bootstrap-server broker:9092