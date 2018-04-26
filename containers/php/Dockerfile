FROM php:7-fpm
RUN apt-get update \
    && apt-get install libpng-dev libfreetype6-dev libjpeg62-turbo-dev -qy \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install gd
