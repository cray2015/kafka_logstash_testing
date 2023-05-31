# __Testing__

- Using multiple Kafka clusters for single logstash. 
- Go to the console of the kafka container and refer the producer commands below and issue the below message, you can change the message.

## __Message__

      {"message": "This is a \"sec-api"}

## __Kafka producer__
kafka-console-producer --topic logstash_logs --bootstrap-server kafka:9092

kafka-console-producer --topic api --bootstrap-server kafka:9092

kafka-console-producer --topic batch --bootstrap-server kafka:9092

## __Kafka-sec producer__
kafka-console-producer --topic sec-logstash --bootstrap-server kafka-sec:9092

kafka-console-producer --topic sec-api --bootstrap-server kafka-sec:9092

      If you push any message in the above topic this should go into "sec-existing.log" file

kafka-console-producer --topic sec-batch --bootstrap-server kafka-sec:9092


## __Check logs__

      In logstash container go to /usr/share/logstash/ and look for topic name log files.

