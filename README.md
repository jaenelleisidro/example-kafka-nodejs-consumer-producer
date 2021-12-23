# example-kafka-nodejs-consumer-producer


modify the directory of the following files

kafka_2.11-2.3.0\config\zookeeper.properties

this contains the dataDir=D:/developer/kafka/data/zookeeper
change this to the correct path

kafka_2.11-2.3.0\config\server.properties

this contains the log.dirs=D:/developer/kafka/data/kafka
change this to the correct path


now that we're ready,lets start running kafka

go to windows folder here
kafka_2.11-2.3.0\bin\windows

open command prompt and run zookeper server by typing this
zookeeper-server-start.bat ../../config/zookeeper.properties

open command prompt and run kafka server by typing this
kafka-server-start.bat ../../config/server.properties



kafka should be running by now, 
next is to run a node js app that produce events and another that consumes the event


return to the root folder then open nodejs folder
you will see producer.js and consumer.js

run both of them by typing this in command prompt
node consumer.js
node producer.js

the producer.js will create an api server at http://localhost:3000/
visit that and it should say, "we sent message to kafka" together with the message sent.

check consumer.js command prompt and it should've logged the message on the console.

references
https://www.goavega.com/install-apache-kafka-on-windows/
https://kafka.js.org/docs/getting-started