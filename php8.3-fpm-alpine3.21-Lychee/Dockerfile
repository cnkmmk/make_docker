FROM php:8.3.14-fpm-alpine3.21
LABEL maintainer="mercuryhg <docker@cnkmmk.eu.org>"

RUN ( curl -sSLf https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions -o - || echo 'return 1' ) | sh -s \
    bcmath exif gmp intl pdo_mysql zip gd imagick mysqli && \
    cp /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini && \
    sed -i 's/max_execution_time = 30/max_execution_time = 200/g' /usr/local/etc/php/php.ini && \
    sed -i 's/post_max_size = 8M/post_max_size = 100M/g' /usr/local/etc/php/php.ini && \
    sed -i 's/upload_max_filesize = 2M/upload_max_filesize = 100M/g' /usr/local/etc/php/php.ini && \
    sed -i 's/memory_limit = 128M/memory_limit = 256M/g' /usr/local/etc/php/php.ini && \
    sed -i 's/;date.timezone =/date.timezone = Asia\/Shanghai/g' /usr/local/etc/php/php.ini
