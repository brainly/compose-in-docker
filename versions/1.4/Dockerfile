FROM alpine:3.2
MAINTAINER Oleksii Fedorov <oleksii.fedorov@brainly.com>

RUN apk update
RUN apk add py-pip

ENV DOCKER_COMPOSE_VERSION=docker-compose==1.4.2

RUN pip install $DOCKER_COMPOSE_VERSION
