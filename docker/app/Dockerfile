FROM php:7.4-fpm
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
        libpq-dev \
        libzip-dev \
    && docker-php-ext-install pdo_pgsql pgsql zip \
    && docker-php-ext-install opcache

COPY ./conf.d/opcache.ini /usr/local/etc/php/conf.d/opcache.ini
COPY . /sandbox
WORKDIR /sandbox
