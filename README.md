# kafka-demo
Kafka practice with CLI and SpringBoot App - Learning and Development


Steps to download and commands to use to run Kafka on windows.

1. Use the link to downlaod the latest version of kafka https://www.apache.org/
2. Unzip the file to a desired location on the system.
3. Set KAFKA_HOME path in the env varibales.
4. Navigate to the path of the kafka file run the commands in the follwing order to get the CLI working.
   1. First Start the Zookeeper - Zookeeper is a like a internal kafka manager - managers kafka servers and configures producer and consumer.
      cmd: .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
   2. Verify to see if the Zookeeper is up on port 2181
5. Open a new cmd promt and navigate to the kafka file run the commands
   cmd : .\bin\windows\kafka-server-start.bat .\config\server.properties
6.Open a new cmd promt and navigate to the kafka file run the commands
  1. Declare a topic 
   cmd : .\bin\windows\kafka-topics.bat --create --topic topic-example --bootstrap-server localhost:9092
  2. Produce to the topic
     cmd : .\bin\windows\kafka-console-producer.bat --topic topic-example --bootstrap-server localhost:9092
     >Hello Kafka
     >Hello World
     >Hello from the other side
     >kafka events
     >Over and Out!!
  4. Read from the topic
     cmd : .\bin\windows\kafka-console-consumer.bat --topic topic-example --from-beginning --bootstrap-server localhost:9092
     cmd : .\bin\windows\kafka-console-consumer.bat --topic topic-example --from-beginning --max-messages 3 --bootstrap-server localhost:9092
     
   


