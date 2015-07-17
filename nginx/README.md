
Building:

```
docker build -t ripta/nginx-alpine:v1.0 .
```

Using:

```
docker run -d -P --name web -v /Users/rpasay/Projects/docker/alpine-nginx/test-root:/srv/www ripta/alpine-nginx:v1.0
docker port web
```

Stopping:

```
docker stop web
docker rm web
```

