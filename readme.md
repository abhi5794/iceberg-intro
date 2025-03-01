# Directions

To start up the different containers individually.

spark 3.3 with jupyter notebook

```
docker-compose up notebook
```

minio (s3-compatible storage layer)

```
docker-compose up minio
```

nessie (transactional catalog for Apache Iceberg)

```
docker-compose up nessie
```

Dremio (data lakehouse platform (query engine, access layer, more))

```
docker-compose up dremio
```

There are three folders in this repo mapped specifically to the spark/notebook container which are:

- `datasets` use this for any sample datasets
- `notebooks` for storing notebooks
- `warehouse` to be used as a warehouse for written data

[Find Guides and Tutorials Here](https://github.com/developer-advocacy-dremio/quick-guides-from-dremio)

For permission errors
```
sudo chmod -R 775 ./notebooks
sudo chown -R 1000:1000 ./notebooks
```

To close the docker compose
```
docker compose down
```
Dremio on localhost:9047
Flink on localhost:8081
Minio on localhost:9001 (storage:9000 for s3 endpoints)
Jupyter Notebook w/ Spark on localhost:8080
