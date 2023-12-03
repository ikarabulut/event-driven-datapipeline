# Event Driven Pipeline with Kafka and Python

**How to start Kafka and Zookeeper:**

- `docker-compose up -d`
- Running the command above should start Kafka and Zookeeper in the background.

**How to check that the containers are running:**

- `docker ps`
- The command above prints all of the running docker containers, I expect to see a container for Kafka and one for Zookeeper running.

**Now in the same directory:**
To consume messages from a topic called `test`:

```
docker-compose exec -it kafka  /opt/bitnami/kafka/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test --from-beginning
```

**To produce messages in a different console run:**

```
poetry run python3 producer.py worker
```

Now you should send messages being produced from the `producer.py` script and showing up in the consumer window!
