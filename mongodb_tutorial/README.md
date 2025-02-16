# CS4221 Mongodb Tutorial

## Priliminary

1. Anaconda (mini-conda is recommended)
2. Docker



## SetUp



**1. Python Virtual Environment**
Create virtual environment by provided `environment.yml`.

```bash
conda env create -f environment.yml
```



**2. Mongodb Server Setup**

Run Mongodb Server as a Docker container using the MongoDB image opensource maintained by the Dcoker Community (instead of mongo db official image).

Pull the MongoDB Docker Image (specific version).

```bash
docker pull mongo:8.0-rc
```

 Start a **mongo** server instance

```shell
docker run -p 27017:27017  --name mongo-server -d mongo:8.0-rc

docker ps | grep mongo-server
# it will print the status of running container.
```

Verify the status of mongodb server through mongosh in container.

```bash
docker exec -it mongo-server mongosh --eval "db.runCommand({hello: 1})"
```

The result of this command returns a document describing your server deployment.

```json
{
  isWritablePrimary: true,
  topologyVersion: {
    processId: ObjectId('67b17e055007558c9068fd2e'),
    counter: Long('0')
  },
  maxBsonObjectSize: 16777216,
  maxMessageSizeBytes: 48000000,
  maxWriteBatchSize: 100000,
  localTime: ISODate('2025-02-16T06:05:26.427Z'),
  logicalSessionTimeoutMinutes: 30,
  connectionId: 5,
  minWireVersion: 0,
  maxWireVersion: 25,
  readOnly: false,
  ok: 1
}
```



## Tutorial

there are three python notebook files to introduce basic operations in mongodb.

- hello_mongodb.ipynb
