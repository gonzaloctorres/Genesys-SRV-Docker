ARG PHP_VERSION
FROM php:$PHP_VERSION-fpm-alpine

COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/bin/

RUN apk update \
    upgrade;

RUN install-php-extensions gd zip mysqli pdo pdo_mysql mcrypt calendar bcmath imap

RUN cd ~ \
    && curl -sS https://getcomposer.org/installer -o composer-setup.php \
    && php composer-setup.php --install-dir=/usr/local/bin --filename=composer

RUN apk add --update --no-cache git bash;

RUN git --version;