# CS4221 Time Series Database Tutorial (InfluxDB)

## SetUp

**InfluxDB server**

We recommend to utilize the docker-compose file provided by us.  

At the begining, we need to create some configuration files.

```shell
$ echo "admin" > ~/.env.influxdb2-admin-username
$ echo "MyInitialAdminPassword" > ~/.env.influxdb2-admin-username
$ echo "MyInitialAdminToken0==" > ~/.env.influxdb2-admin-token
```

then, you can easily start a influxDB server by executing 

```shell
$ docker compose up influxDB2 -d
```

the docker compose will automatically read the configuration files and help you set up the server.

If successful, influxDB initializes the user, password, organization (docs), bucket, and Operator token, and then logs to stdout. You can view the influxDB UI at http://localhost:8086.

> Of course, other methods are also available, please check the influxDB version 2 official [documentation](https://docs.influxdata.com/influxdb/v2/install/) 



**InfluxDB client**

we still choose python and using python driver library to interact with database server.

you can download the `influxdb-client` python package

or you can also create virtual environment by `environment.yml` file we provided.

```shell
$ conda env create -f environment.yml
$ conda env list
$ conda activate cs4221
# cs4221 is the name of virtual environment
```



## Preliminaries

please read the [documentation](https://docs.influxdata.com/influxdb/cloud/reference/key-concepts/) and learn about the key concept, such as `Point`, `Measurement`, `Tag`, `Field`  

and follow `hello_influxdb.ipynb` and try some basic operation in influxDB





## Tutorial

there are three python notebook files to introduce basic operations in influxDB.

- hello_influxdb.ipynb
- hello_influxdb_2.ipynb
- hello_influxdb_3.ipynb

the next two tutorials are about specific dataset, you need to download related dataset first.

We recommend you to execute the queries appearing in these notebook in InfluxDB UI which will visualize the data and help data analysis. 
