FROM php:8.3-fpm-alpine

# postgres
RUN apk add --no-cache libpq-dev npm && docker-php-ext-install pdo_pgsql

COPY ./app /var/www/html

WORKDIR /var/www/html

COPY --from=composer/composer:latest-bin /composer /usr/bin/composer

EXPOSE 9000

