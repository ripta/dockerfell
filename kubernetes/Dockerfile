# Dockerfile
# image: ripta/kubernetes:v0.21.1-1.0

FROM gliderlabs/alpine:3.1
MAINTAINER Ripta Pasay <ripta+docker@pasay.name>

RUN apk update
RUN apk add bash
RUN apk add build-base curl rsync
RUN apk add git
RUN apk add go

RUN mkdir -p /go
ENV GOROOT /usr/lib/go
ENV GOPATH /go
ENV PATH $PATH:$GOROOT/bin:$GOPATH/bin

ENV KUBERNETES_VERSION v0.21.1

RUN mkdir /build
RUN mkdir /kubernetes

WORKDIR /build
RUN go get github.com/tools/godep
RUN git clone git://github.com/GoogleCloudPlatform/kubernetes --depth 1 --branch $KUBERNETES_VERSION

WORKDIR /build/kubernetes
RUN hack/build-go.sh
RUN mv _output/local/go/bin/* /kubernetes/

VOLUME /kubernetes

