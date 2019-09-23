FROM rajivnix/php:7.1.19

WORKDIR /var/www
RUN docker-php-ext-install pdo pdo_mysql pcntl posix
RUN apt-get update && apt-get install -y nginx supervisor \
    && rm -rf /var/lib/apt/lists/* \
    && rm -rf /etc/nginx/sites-enabled/* && rm -rf /etc/nginx/sites-available/*

COPY  ./docker-utils/supervisord/start-services.sh /usr/local/bin/start-services.sh
RUN chmod 777 /usr/local/bin/start-services.sh
COPY ./docker-utils/nginx/conf.d/app.conf /etc/nginx/conf.d/app.conf

COPY docker-utils/supervisord/*.conf /etc/supervisor/conf.d/

COPY . /var/www
ENTRYPOINT ["/usr/local/bin/start-services.sh"]
