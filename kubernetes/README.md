
Build them binaries:

```
cd kubernetes
docker build -t ripta/kubernetes:v0.21.1-1.0 .
```

Run a container using the image and note down the container ID:

```
docker run -d ripta/kubernetes:v0.21.1-1.0 sh
```

Copy the `/kubernetes` directory from the container, and then destroy it:

```
docker cp $CONTAINER_ID:/kubernetes/ .
docker rm $CONTAINER_ID
```

Package things up:

```
cd kubernetes
tar zcf ../kubernetes-v0.21.1-1.0.tar.gz .
```

