## **To Download Kafka**

- [To install kafka](https://kafka.apache.org/downloads)


## PREREQUITES  
- Java

**To create a Topic**

```
./kafka-topics.sh --create --topic my-topic --bootstrap-server localhost:9092 --replication-factor 1 --partitions 3
```

**PRODUCER SENDING MESSAGES**

```
./kafka-console-producer.sh --broker-list localhost:9092 --topic my-topic
```

![image](https://github.com/user-attachments/assets/e5a6a3bc-26de-4437-bc68-1a4bd9a98313)

**CONSUMER-1 RECEIVING MESSAGES FROM BEGINNING**

![image](https://github.com/user-attachments/assets/a9aae8e9-1518-4bdb-9fe2-1dc81d6d7772)

**CONSUMER-2 RECEIVING MESSAGES FROM BEGINNING**

```
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic my-topic --from-beginning
```

![image](https://github.com/user-attachments/assets/955a52ae-1d69-4bc1-a8f5-80a7e0805df2)
