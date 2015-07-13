
# Dockerfell

A collection of Dockerfiles for various things that do not have a home of their
own yet.

## Obtain Docker

Install docker if you haven't already. On OS X, the method I prefer is to
utilize Homebrew:

1. `brew install docker`
2. `brew install docker-machine`
3. `docker-machine help create` and look for the `--driver` option for all
   possible values
4. `docker-machine create --driver vmwarefusion dev` or with whatever driver
   you use
5. `eval $(docker-machine env dev)` to allow your local docker client to
   connect to the docker running inside the virtual machine
6. `docker ps` to check that your docker can connect
7. Go into the directory you want, which contains a `Dockerfile`, and check out
   its `README` file.

## Test Image

Pull down a small image to testdrive your setup:

1. Ensure that your environment variables are setup: `env | grep DOCKER`;
   otherwise, `eval $(docker-machine env dev)`
2. `docker run -i -t gliderlabs/alpine:3.1 /bin/sh`
3. And now you'll be placed inside an ephemeral machine
4. Exit the shell to stop the container; none of your changes will be kept


