FROM php:7.0-fpm

RUN apt-get update && apt-get install -y libjpeg-dev libpng12-dev
RUN docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr
RUN docker-php-ext-install mysqli
