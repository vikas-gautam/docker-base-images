# Example Nodejs PHP image
This is Example php golden image and is based on Example Golden Image(rajivnix/debian8-base) with php-fpm and
this image can be paired with webservers to serve applications which required
php.

Any changes made to the Dockerfile of this image needs a new image to be built and
pushed to docker registry(ECR). This process would be done via an CI/CD in future.

```
docker build -t rajivnix/php:7.1.19 .
docker push rajivnix/php:7.1.19
```

# Configuring your application containers
Any node-js based application would use this images as source. For example you could add
in docker-compose.yml file

```
mynodecontainer:
    source: rajivnix/php:7.1.19
    environment:
    ...
```