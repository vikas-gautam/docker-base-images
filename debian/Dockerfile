FROM debian:8-slim
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && \
    apt-get install -y --no-install-recommends apt-utils wget curl vim openssl git software-properties-common \
    && rm -rf /var/lib/apt/lists/*
