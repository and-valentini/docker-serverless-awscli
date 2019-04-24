FROM node:8.4-alpine
RUN apk --no-cache add python python3 python3-dev py-pip ca-certificates groff less bash make jq curl wget g++ zip git openssh && \
    pip --no-cache-dir install awscli && \
    update-ca-certificates

RUN npm i -g serverless --unsafe-perm
EXPOSE 3000 8000
WORKDIR /opt/app