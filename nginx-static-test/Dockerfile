FROM alpine:3.2
MAINTAINER Ripta Pasay <ripta+docker@pasay.name>

ENV META_IMAGE_VERSION 1.0

RUN apk update
RUN apk add nginx

COPY . /usr/share/nginx/html/
RUN echo "Generated at $(date)" > /usr/share/nginx/html/VERSION

EXPOSE 80
