##
## Name: docker-lemp-7.4
## Author: https://about.me/henrycv
##

FROM php:7.4.7-fpm-alpine3.12

RUN apk add --no-cache libzip-dev && \
  docker-php-ext-configure zip  && \
  docker-php-ext-install zip

RUN docker-php-ext-install mysqli  && \
  docker-php-ext-install pdo_mysql pcntl

RUN apk add --no-cache libpng libpng-dev && \
  docker-php-ext-install gd && \
  apk del libpng-dev


# Install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer