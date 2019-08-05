
FROM php:7.1-fpm

# install dependencies
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libmcrypt-dev \
        libpng-dev \
        libjpeg-dev \
        libpng-dev 

#install php extension
RUN docker-php-ext-install iconv mcrypt \

#config gd and install
RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
RUN docker-php-ext-install gd


FROM wyveo/nginx-php-fpm:latest