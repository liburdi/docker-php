FROM php:7.4-fpm
ADD https://github.com/phpredis/phpredis/archive/3.1.4.tar.gz /tmp/redis.tar.gz
RUN tar xzf /tmp/redis.tar.gz -C /tmp \
    && mkdir -p /usr/src/php/ext \
    && mv /tmp/phpredis-3.1.4 /usr/src/php/ext/redis \
    && echo 'redis' >> /usr/src/php-available-exts \
    && docker-php-ext-install redis \
    && rm -rf /usr/src/php/ext/redis
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer
RUN composer config -g repo.packagist composer https://packagist.phpcomposer.com
RUN docker-php-ext-install pdo_mysql
RUN apt-get update  && apt-get install -y libmcrypt-dev
RUN apt-get install -y vim && apt-get -y install zlib1g zlib1g-dev
EXPOSE 9000