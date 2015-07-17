FROM gliderlabs/alpine:3.1
MAINTAINER Ripta Pasay <ripta+docker@pasay.name>

ENV DOCKER_NGINX_VERSION 1.6.2-r1
RUN apk-install nginx
RUN mkdir -p /tmp/nginx/client-body

ADD nginx.conf /etc/nginx/nginx.conf

VOLUME /srv/www

EXPOSE 80

ENTRYPOINT ["nginx"]

