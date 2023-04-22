FROM php:7.4.2-fpm

RUN cd /usr/bin && curl -s http://getcomposer.org/installer | php && ln -s /usr/bin/composer.phar /usr/bin/composer

RUN apt-get update
RUN apt-get install -y git libzip-dev vim
RUN docker-php-ext-install zip
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install pdo_mysql
# RUN pecl install redis \
#     && docker-php-ext-enable redis

# RUN pecl install xdebug-3.0.0 \
#   && docker-php-ext-enable xdebug