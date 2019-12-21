ARG BASE_IMAGE=drupalwxt/site-wxt:latest
FROM $BASE_IMAGE

COPY php.ini /usr/local/etc/php/php.ini

## START CI

WORKDIR /var/www


RUN php -r "opcache_reset();"


WORKDIR /var/www/html
