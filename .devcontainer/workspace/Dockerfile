FROM mcr.microsoft.com/devcontainers/base:jammy

ENV TZ Asia/Tokyo
ENV PHP_VERSION 7.3

RUN apt-get update &&\
    apt-get install -y software-properties-common &&\
    add-apt-repository ppa:ondrej/php -y &&\
    apt-get install -y \
        php${PHP_VERSION} \
        php${PHP_VERSION}-json \
        php${PHP_VERSION}-mysqlnd \
        php${PHP_VERSION}-curl \
        php${PHP_VERSION}-dom \
        php${PHP_VERSION}-exif \
        php${PHP_VERSION}-fileinfo \
        php${PHP_VERSION}-igbinary \
        php${PHP_VERSION}-imagick \
        php${PHP_VERSION}-intl \
        php${PHP_VERSION}-mbstring \
        php${PHP_VERSION}-xml \
        php${PHP_VERSION}-zip  &&\
    apt-get clean &&\
    rm -rf /var/lib/apt/lists/*

COPY --from=composer /usr/bin/composer /usr/bin/composer