This repository hosts the instructions and neccessary artifacts for building and publishing Python Functions as a Docker container on Linux.

For comprehensive information about Python in Azure Functions, refer to the [azure-functions-python-worker](https://github.com/Azure/azure-functions-python-worker) repo.

# Getting Started

## Prerequisites

* [Git](https://git-scm.com/downloads)
* An active [Azure subscription](https://azure.microsoft.com/pricing/free-trial/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=docs&utm_campaign=visualstudio)
* [Docker](https://docs.docker.com/get-started/#setup)
* A [Docker Hub account](https://docs.docker.com/docker-id/)

## Download the sample

In a terminal window, run the following command to clone the sample app repository to your local machine, then change to the directory that contains the sample code.

```bash
git clone https://github.com/Azure/azure-functions-docker-python-sample.git
cd azure-functions-docker-python-sample
```

## Understanding the environment

In the Git repository, take a look at the `Dockerfile`. This file describes the environment that is required to run Python functions on Linux. 

```dockerfile
# Base the image on the built-in Azure Functions Python image
FROM microsoft/azure-functions-python3.6:v2.0.11737-alpha

# Add files from this repo to the root site folder.
COPY . /home/site/wwwroot

# Install requirements
RUN cd /home/site/wwwroot && pip install -r requirements.txt
```

## Build and deploy the custom image

https://wikiazure.com/devops/azure-devops-automate-your-release-pipeline-to-provision-a-docker-container-to-azure-web-app-for-containers/



![releasepipeline](https://user-images.githubusercontent.com/48413770/89361577-408ff680-d691-11ea-857e-c98510e84b44.JPG)


Container Registry 
![image](https://user-images.githubusercontent.com/48413770/89361685-7df48400-d691-11ea-94d9-c4adea75a3ce.png)




