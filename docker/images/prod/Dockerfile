ARG BASE_IMAGE=drupalwxt/site-wxt:latest
FROM $BASE_IMAGE

COPY php.ini /usr/local/etc/php/php.ini
COPY html/sites/default/conf/drupal/settings.php /var/www/html/sites/default/settings.php:ro
## START CI

WORKDIR /var/www


RUN php -r "opcache_reset();"


WORKDIR /var/www/html
