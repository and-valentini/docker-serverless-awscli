# AWS API Gateway Example

Greeting API using AWS Gateway and Lambda.

## Pre-requisites

- Docker
- Docker Compose
  > Environment variables can be defined inside your shell session using `export VAR=value` or setting them in .env file. See `.env.example` for more information.

## Usage

```bash
# build lambda package
$ make build

# deploy to aws
$ make deploy

# remove the api gateway
$ make remove

# clean your folder
$ make _clean

# PS: this project use custom aws cli configuration folder if you want to use the local aws cli configuration folder replace:
 aws:/root/.aws

# with:
 ~/.aws:/root/.aws

# in whole project
```
