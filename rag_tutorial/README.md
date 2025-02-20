# CS4221 RAG Tutorial

## Priliminary

1. Anaconda (mini-conda is recommended)
2. Docker


## SetUp

**1. Notebook Virtual Environment**

you can create virtual environment by `environment.yml` file we provided under this directory.

```bash
conda env create -f environment.yml
```

Make sure the `environment.yml` is the latest version. Otherwise delete the old environment and create a new one.

this environment involves *langchain* and *huggingface* dependecies, which may take some time to install.
```bash
conda env remove -n cs4221
```


**2. Large Language Model Setup**

We need a LLM to support our RAG model. Of course, we can directly use the LLM service provided by OpenAI or DeepSeek, but it's not free.

There, we choose to deploy a mini-LLM llama in our local machine. The llama is a small version of GPT-2, which is enough for our tutorial.

You can check the llama repo [here](https://github.com/ollama/ollama). There are various ways to download.

In this tutorial, we recommend using the docker image. You can pull the image by running the following command:

```bash
docker pull ollama/ollama
```

Then, you can run the image by:

```bash
docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

choose specific version of model for service:
    
```bash
docker exec -it ollama ollama run llama3.2
# 2GB model, you can refer https://github.com/ollama/ollama, choose which model your local computer can handle.
```

## Tutorial
`rag_example.ipynb` provides a basic example of how to build RAG application above on our own datasets. You can refer to the notebook for more details.