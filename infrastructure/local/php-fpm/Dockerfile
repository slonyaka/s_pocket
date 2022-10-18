FROM php:8.1-fpm

ARG APP_DEBUG=false

RUN  docker-php-ext-install mysqli pdo pdo_mysql && docker-php-ext-enable mysqli pdo_mysql

# xdebug
RUN if [ ${APP_DEBUG} ] ; then (pecl install xdebug-3.1.5 && docker-php-ext-enable xdebug ); fi

# redis
RUN pecl install redis-5.3.4 && docker-php-ext-enable redis
