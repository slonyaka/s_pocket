FROM php:8.1-fpm

RUN  docker-php-ext-install mysqli pdo pdo_mysql && docker-php-ext-enable mysqli pdo_mysql

# xdebug
RUN pecl install xdebug-3.1.5 && docker-php-ext-enable xdebug
COPY docker-php-ext-xdebug.ini /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini

# redis
RUN pecl install redis-5.3.4 && docker-php-ext-enable redis



EXPOSE 9000
