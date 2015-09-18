FROM ripta/nodejs:0.12.2
MAINTAINER Ripta Pasay <ripta+docker@pasay.name>

ENV META_IMAGE_VERSION 1.4.0
ENV BUILD_HOME /app

RUN apk update
RUN apk add python make g++

RUN mkdir -p $BUILD_HOME
VOLUME ["/app"]
WORKDIR $BUILD_HOME

