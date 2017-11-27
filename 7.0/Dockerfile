FROM php:7.0
LABEL maintainer="MilesChou <jangconan@gmail.com>"

ENV SWOOLE_VERSION=1.9.23

# Compile Swoole
RUN set -xe && \
        curl -LO https://github.com/swoole/swoole-src/archive/v${SWOOLE_VERSION}.tar.gz && \
        tar xzf v${SWOOLE_VERSION}.tar.gz && \
        cd swoole-src-${SWOOLE_VERSION} && \
            phpize && \
            ./configure && \
            make -j && \
            make && \
            make install && \
        docker-php-ext-enable swoole && \
        cd ../.. && rm -rf v${SWOOLE_VERSION}.tar.gz swoole-src-${SWOOLE_VERSION} && \
        php -m
