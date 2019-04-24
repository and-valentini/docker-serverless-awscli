# andvalentini/serverless-awscli

Docker image containing NodeJS, Serverless Framework and AWS cli. And an example for using it with docker-compose


[base image Readme](base_image/README.md)

[example project Readme](project/README.md)

## Notes
this project use custom aws cli configuration folder if you want to use the local aws cli configuration folder.
```bash
# replace:
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

## Example

`project/apigw` is an example on how to use `andvalentini/serverless-awscli`.
