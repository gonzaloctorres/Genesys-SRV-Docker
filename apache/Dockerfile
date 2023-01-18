ARG APACHE_VERSION
FROM httpd:$APACHE_VERSION-alpine

RUN apk update; \
    apk upgrade;

RUN apk add \
  bash \
  apache2 \
  php8-apache2 \
  curl \
  ca-certificates \
  openssl \
  git \
  php8 \
  php8-phar \
  php8-json \
  php8-iconv \
  php8-openssl \
  tzdata \
  openntpd \
  php8-ftp \
  php8-xdebug \
  php8-pecl-mcrypt \
  php8-mbstring \
  php8-soap \
  php8-gmp \
  php8-pdo_odbc \
  php8-dom \
  php8-pdo \
  php8-zip \
  php8-bcmath \
  php8-gd \
  php8-odbc \
  php8-pdo_mysql \
  php8-gettext \
  php8-xmlreader \
  php8-xmlwriter \
  php8-tokenizer \
  php8-xml \
  php8-bz2 \
  php8-pdo_dblib \
  php8-curl \
  php8-ctype \
  php8-session \
  php8-exif \
  php8-pear \
  php8-dev \
  gcc \
  nodejs;

RUN sed -i "s/#LoadModule\ rewrite_module/LoadModule\ rewrite_module/" /usr/local/apache2/conf/httpd.conf;

RUN mkdir -p /var/www/vhosts

COPY ambientes.conf /usr/local/apache2/conf/ambientes.conf
RUN echo "Include /usr/local/apache2/conf/ambientes.conf" \
    >> /usr/local/apache2/conf/httpd.conf