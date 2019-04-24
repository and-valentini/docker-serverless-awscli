# andvalentini/serverless-awscli

Docker image containing NodeJS, Serverless Framework and AWS cli.

## Usage

```bash
# build:
 docker build -t $(IMAGE_NAME) .

# Open bash:
 docker run --rm -it -v $(pwd):/opt/app -v $(pwd)/aws:/root/.aws -v ~/.ssh:/root/.ssh $(IMAGE_NAME) bash

# Run serverless deploy in the image: open bash with command above and then:
 sls deploy

# PS: this project use custom aws cli configuration folder if you want to use the local aws cli configuration folder replace:
 aws:/root/.aws

# with:
 ~/.aws:/root/.aws

# in whole project
```

## Docker image

The Docker image has the following:

- Node 8.4 (Alpine)
- [Serverless Framework](https://serverless.com)
- [AWS CLI](https://github.com/aws/aws-cli): required by some Serverless plug-ins to work