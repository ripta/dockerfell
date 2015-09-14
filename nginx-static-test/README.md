
Building:

```
docker build -t your-username/nginx-static-test:1.0 .
```

Using:

```
docker run -d -p 80 ripta/nginx-static-test:1.0 nginx -g 'daemon off;'
```

