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
