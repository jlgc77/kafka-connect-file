# Kafka Connect. Kafka 2.3 and Maven. 
# Read and writer from local file

Connector based on the official Kafka documentation.

But created with maven instead of gradle.

## Installation

We download kafka, and unzip it wherever you want. It is my case the version I have used is:
 - kafka_2.12-2.3.0.tgz

From the root folder where we have unzipped kafka, we start Zookeeper and Kafka:

 - bin/zookeeper-server-start.sh config/zookeeper.properties
 - bin/kafka-server-start.sh config/server.properties
 - 
We leave the project https://github.com/jlgc77/kafka-connect-file, and we package it.
 - mvn clean package
 
We add the project to CLASSPATH:

 - export CLASSPATH=<path-proyect>/target/kafka-connect-file.jar

From the root path of the project, start the connector:

 - `<path-kafka>`/bin/connect-standalone.sh config/connect-standalone.properties config/connect-file-source.properties
 
In the root folder of the project we add data to the file, it is not necessary to create the file, when executing the command below, it will be created automatically.

 - echo `date` >> test.txt

We create a consumer of the topic, it is not necessary to create the topic before, it will be created automatically when necessary

 -  `<path-kafka>`/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic connect-test --from-beginning
