# kafka

## start kafka docker image
sudo docker-compose up -d

## create kafka topic 
/bin/kafka-topics --create --topic my-events --bootstrap-server localhost:9092

## produce messages to a given topic
/bin/kafka-console-producer --topic my-events --bootstrap-server localhost:9092
event 1  
event 2  
event 3  
event4  
<ctrl+c>

## consume all messages from the topic
/bin/kafka-console-consumer --topic my-events --from-beginning --bootstrap-server localhost:9092

## consume messages with a given offset
/bin/kafka-console-consumer --topic my-events --offset 10 --partition 0 --bootstrap-server localhost:9092

## number of messages in the topic
/bin/kafka-run-class kafka.tools.GetOffsetShell --broker-list localhost:9092 --topic my-events

