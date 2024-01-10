FROM php:8.3-fpm-alpine

RUN apk add supervisor libzip-dev git zip oniguruma-dev \
        mysql-client autoconf libpng-dev imap-dev openssl-dev \
  && docker-php-ext-install zip mbstring mysqli pdo_mysql

COPY ./app /var/www/html

WORKDIR /var/www/html

COPY --from=composer/composer:latest-bin /composer /usr/bin/composer

EXPOSE 9000

