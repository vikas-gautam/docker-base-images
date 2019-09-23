FROM rajivnix/debian8-base

RUN apt-get update && apt-get install -y nginx \
    && rm -rf /var/lib/apt/lists/* \
    && rm /etc/nginx/sites-enabled/default
COPY docker-utils/conf/nginx.conf /etc/nginx/nginx.conf
COPY docker-utils/conf/app.conf /etc/nginx/conf.d/app.conf
EXPOSE 80 443
CMD ["nginx", "-g", "daemon off;"]
