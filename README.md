kafka-client
-----

[Docker HUB link](https://hub.docker.com/r/incu6us/kafka-client)

#### Usage:

Produce:

```console
docker run -ti --rm incu6us/kafka-client kafka-console-producer.sh --topic mega-topic --broker-list 172.16.0.1:9094
```


Consume:

```console
docker run -ti --rm incu6us/kafka-client kafka-console-consumer.sh --topic mega-topic --bootstrap-server 172.16.0.1:9094
```


Create topic:

```console
docker run -ti --rm incu6us/kafka-client kafka-topics.sh --create --bootstrap-server 172.16.0.1:9094 --replication-factor 1 --partitions 1 --topic mega-topic
```


List group:

```console
docker run -ti --rm incu6us/kafka-client kafka-consumer-groups.sh --bootstrap-server 172.16.0.1:9094 --list
```


Describe group:

```console
docker run -ti --rm incu6us/kafka-client kafka-consumer-groups.sh --bootstrap-server 172.16.0.1:9094 --group test-group --describe
```
