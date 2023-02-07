FROM php:7.4-fpm

# Installing dependencies for the PHP modules
RUN apt-get update && apt-get install -y zip libzip-dev libpng-dev libicu-dev libonig-dev libcurl4-gnutls-dev libxml2-dev

# Installing additional PHP modules
RUN docker-php-ext-install mysqli pdo pdo_mysql gd zip bcmath ctype intl mbstring opcache xml dom curl
RUN echo '\nmemory_limit = 2048M;' >> /usr/local/etc/php/php.ini;
RUN echo '\nerror_reporting=E_ERROR;' >> /usr/local/etc/php/php.ini;
RUN echo '\nshort_open_tag=On;' >> /usr/local/etc/php/php.ini;
