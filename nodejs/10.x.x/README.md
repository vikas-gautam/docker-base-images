# Example Nodejs Golden image(v10.16.1)
This is Example Nodejs golden image and is based on Example Golden Image(rajivnix/debian8-base).

Any changes made to the Dockerfile of this image needs a new image to be built and
pushed to docker registry(ECR). This process would be done via an CI/CD in future.

```
docker build -t rajivnix/nodejs:10.16.1 .
docker push rajivnix/nodejs:10.16.1
```

# Configuring your application containers
Any node-js based application would use this images as source. For example you could add
in docker-compose.yml file

```
mynodecontainer:
    source: rajivnix/nodejs:10.16.1
    environment:
    ...
```
