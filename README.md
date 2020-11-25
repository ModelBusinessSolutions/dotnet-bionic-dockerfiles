### How to update each image
In order to update and push new images to dockerhub, you have to build, tag and push each image with the following order as each image is dependent on the previous one:

<a href="https://hub.docker.com/repository/docker/modelerp/runtime-deps">runtime-deps</a> -> <a href="https://hub.docker.com/repository/docker/modelerp/runtime">runtime</a> -> <a href="https://hub.docker.com/repository/docker/modelerp/aspnet">aspnet</a> -> <a href="https://hub.docker.com/repository/docker/modelerp/sdk">sdk</a>

```
cd runtime-deps
docker build -t runtime-deps:5.0.0-bionic-amd64 .
docker tag runtime-deps:5.0.0-bionic-amd64 modelerp/runtime-deps:5.0.0-bionic-amd64
docker push modelerp/runtime-deps
```

