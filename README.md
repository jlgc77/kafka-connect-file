
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
