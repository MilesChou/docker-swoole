FROM php:7.3

LABEL maintainer="MilesChou <jangconan@gmail.com>"

ENV SWOOLE_VERSION=4.3.4

RUN set -xe && \
        pecl install swoole-${SWOOLE_VERSION} && \
        docker-php-ext-enable swoole && \
        php -m
