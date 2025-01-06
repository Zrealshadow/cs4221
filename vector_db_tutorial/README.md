# CS4221 Vector Database Tutorial

## Priliminary

1. Anaconda (mini-conda is recommended)
2. Docker

## SetUp

**1. Notebook Virtual Environment**

```bash
# create new virtual environment
conda create -n milvus python=3.9 -y
# activate environment
conda activate milvus
# download pymilvus, refer to https://milvus.io/docs/quickstart.md
pip install -U pymilvus
# download notebook dependency for milvus.
conda install -n milvus ipykernel


# [Optional] if you want to execute the quickStart.ipynb
# install basic model, maybe take some time if your local environment has no Pytorch
pip install pymilvus[model]
```

you can also create virtual environment by `environment.yml` file we provided under this directory.

```bash

**2. Milvus Setup**

The `docker-compose` file provides an easy standalone deployment option in which the milvus version is `2.3.x`.

To change the milvus image: modify the `standalone.image`. To add Go mem control, add to the `standalone.environment`. To change logging, add the `log.level: debug` to `standalone.environment`.



## Tutorial

there are two notebook files to introduce basic operations in milvus.

- quickStart.ipynb
- hello_milvus.ipynb
- float_index_tune.ipynb

