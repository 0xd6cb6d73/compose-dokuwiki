FROM php:7.4-fpm-alpine

RUN apk add tzdata

ENV TZ="Europe/Paris"
RUN cp /usr/share/zoneinfo/Europe/Berlin /etc/localtime
RUN echo "Europe/Paris" >  /etc/timezone

RUN apk add autoconf
RUN apk add libgcc libstdc++
RUN apk add binutils
RUN apk add libgomp
RUN apk add libatomic
RUN apk add libgphobos
RUN apk add gmp isl22
RUN apk add mpfr4 mpc1
RUN apk add gcc
RUN apk add musl-dev libc-dev
RUN apk add g++
RUN apk add make
RUN pecl install redis-5.3.7
RUN docker-php-ext-enable redis

COPY ./redis.ini /usr/local/etc/php/conf.d/redis.ini
COPY ./upload.ini /usr/local/etc/php/conf.d/upload.ini

WORKDIR /var/www/html

LABEL version="1.5-alpine"

EXPOSE 9000
