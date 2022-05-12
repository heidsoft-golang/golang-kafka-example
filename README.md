## Kafka Golang Example

Example code for my [blog post](https://sohamkamani.com/golang/working-with-kafka/).

Steps to run:

1. Clone this repository
2. Install dependencies : `go mod tidy && go mod vendor`
3. Make sure [Kafka is running](https://www.sohamkamani.com/blog/2017/11/22/how-to-install-and-run-kafka/), and change the value of `brokerAddress` to the address of you Kafka instance
4. Run the code : `go run main.go`

> You can see how to install and run a Kafka cluster in my [other tutorial](https://www.sohamkamani.com/blog/2017/11/22/how-to-install-and-run-kafka/)

## 本地测试

```
nohup bin/zookeeper-server-start.sh config/zookeeper.properties >> /data/zookeeper/zookeeper.log &
nohup  bin/kafka-server-start.sh config/server.properties >> /data/kafka-logs/kafka.log &
[root@node1 kafka_2.13-3.1.0]# bin/kafka-topics.sh --bootstrap-server node1:9092,node2:9092,node3:9092 --create --topic test --partitions 3 --replication-factor 1
Created topic test.
[root@node1 kafka_2.13-3.1.0]# 
```

1. https://zhuanlan.zhihu.com/p/512964541?
