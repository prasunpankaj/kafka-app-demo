# kafka-app-demo
# https://www.youtube.com/watch?v=hyJZP-rgooc
# https://www.youtube.com/watch?v=Q4XA5nUpLeo


# Download from here:

https://www.apache.org/dyn/closer.cgi?path=/kafka/3.1.0/kafka_2.13-3.1.0.tgz

# Unzip in following  path:

/Users/pankaj1.prasun/Documents/kafka/bin

# To Start Zookeeper:


./zookeeper-server-start.sh ../config/zookeeper.properties

# To Start kafka Server: Port 9092

./kafka-server-start.sh ../config/server.properties

# To Create Topic:

./kafka-topics.sh **--create --topic test-topic** --bootstrap-server localhost:9092 --replication-factor 1 --partitions 4

./kafka-topics.sh **--create --topic test-topic1** --bootstrap-server localhost:9092 --replication-factor 1 --partitions 4

# To List the Created Topic:
./kafka-topics.sh --list --bootstrap-server localhost:9092 

test-topic
test-topic1

# Now Create Consumer from Console:

./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test-topic --from-beginning
From Start

# Create PRODUCER to Send Message to CONSUMER:

./kafka-console-producer.sh --broker-list localhost:9092 --topic test-topic
> from Start 
