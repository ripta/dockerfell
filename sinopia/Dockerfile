FROM ripta/nodejs:0.12.2
MAINTAINER Ripta Pasay <ripta+docker@pasay.name>

ENV META_IMAGE_VERSION 1.4.0
ENV SINOPIA_HOME /app

EXPOSE 4873

RUN mkdir -p $SINOPIA_HOME
VOLUME ["/app"]

ADD config.yml $SINOPIA_HOME/

CMD ["node", "$SINOPIA_HOME/node_modules/.bin/sinopia"]

