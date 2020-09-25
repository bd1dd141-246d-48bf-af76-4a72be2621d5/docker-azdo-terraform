# docker-azdo-terraform

AzDO build agent in a docker image that has Terraform installed

## Description

Agent is added to the default pool of the AzDO organization targeted. 

[Microsoft documentation](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops) on configuring the build agent in docker

## Usage

from where ever you want to run your docker image:

``` bash
docker build -t dockeragent:latest .
```

``` bash
docker run -e AZP_URL=<Azure DevOps instance> -e AZP_TOKEN=<PAT token> -e AZP_AGENT_NAME=mydockeragent dockeragent:latest
```

In your Azure DevOps pipeline yaml:

``` yaml
pool: default
```
