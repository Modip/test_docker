FROM php:8.1-alpine
RUN apk add --no-cache $PHPIZE_DEPS \
    && pect install xdebug-3.1 \
    && docker-php-ext-eneable xdebug \
    && echo "xdebug.mode=debug" >> /usr/local/php/conf.d/docker-php-ext-xdebug \
    && echo "xdebug.client_host=host.docker.internal" >> /usr/local/php/conf.d/docker-php-ext-xdebug.ini 
WORKDIR /usr/src/webapp
CMD ["php", "-S", "0.0.0.8000"]