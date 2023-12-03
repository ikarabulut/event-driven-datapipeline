# Event Driven Pipeline with Kafka and Python

### Local Setup

This repository utilizes the [Postgres Sample Dataset](https://www.postgresqltutorial.com/postgresql-getting-started/postgresql-sample-database/) to load this you need to apply the following commands after starting the docker container.

```
docker exec {docker container id} sh -c "createdb dvdrental -h localhost -U postgres"
pg_restore -h localhost -p 5432 -U postgres ./dvdrental.tar -d dvdrental
```

Password is `example`
