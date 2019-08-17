FROM php:7.0-fpm
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
    && docker-php-ext-install -j$(nproc) iconv \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd
    && docker-php-ext-install mysqli  
    && docker-php-ext-enable mysqli
#FROM php

#RUN docker-php-ext-install pdo_mysqli && docker-php-ext-install mysqli  && docker-php-ext-enable mysqli && docker-php-ext-install json
#RUN docker-php-ext-install mysqli  && docker-php-ext-enable mysqli && docker-php-ext-install json
