FROM php:8.3.14-fpm-alpine3.21
LABEL maintainer="mercuryhg <docker@cnkmmk.eu.org>"

RUN ( curl -sSLf https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions -o - || echo 'return 1' ) | sh -s \
    bcmath exif gmp intl pdo_mysql zip gd imagick mysqli
