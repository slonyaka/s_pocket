FROM php:8.1-fpm

RUN  docker-php-ext-install mysqli pdo pdo_mysql && docker-php-ext-enable mysqli pdo_mysql

# xdebug
RUN if [ $APP_DEBUG ] ; then (pecl install xdebug-3.8.1 && docker-php-ext-enable xdebug ); fi

# redis
RUN pecl install redis-5.3.4 && docker-php-ext-enable redis
