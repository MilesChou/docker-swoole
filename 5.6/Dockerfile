FROM php:5.6

LABEL maintainer="MilesChou <jangconan@gmail.com>"

ENV SWOOLE_VERSION=1.10.5

RUN set -xe && \
        pecl install swoole-${SWOOLE_VERSION} && \
        docker-php-ext-enable swoole && \
        php -m
