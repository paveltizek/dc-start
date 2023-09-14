ARG INSTALL_CRON=1
ARG INSTALL_COMPOSER=1
ARG PHP_VERSION
ARG GLOBAL_VERSION
FROM thecodingmachine/php:8.2.10-v4-fpm


COPY ./ /var/www/html/

WORKDIR /var/www/html/

ENV PHP_INI_DIR "/usr/local/etc/php"

RUN #pecl install xdebug \
#    && docker-php-ext-enable xdebug

RUN  echo "zend_extension=$(find $(php-config --extension-dir) -name xdebug.so)" \
         > /usr/local/etc/php/conf.d/xdebug.ini