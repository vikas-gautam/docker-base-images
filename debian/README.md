# Example Golden Image

This is Example Golden Image and is based on debian:8-slim. This image should be used to
create futher golden images. Currently we have following golden images which are based on this
* Example Nodejs golden image
* Example php golden image
* Example nginx golden image
* Example Java golden image

In case any new golden image needs to be based out of this add this in the Dockerfile

```
FROM rajivnix/debian8-base
```

In case any change is made in the Dockerfile of this image, a new image needs to be built and pushed to
docker registry(ECR). This process would be automated via a CI/CD process.

```
docker build -t rajivnix/debian8-base:latest .
docker push rajivnix/debian8-base:latest
```