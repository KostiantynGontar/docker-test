FROM ubuntu

MAINTAINER Konstantin Gontar <gontarkonstantin@gmail.com>

RUN apt-get update && apt-get install -qy php5-cli php5-common php5-mysql php5-gd php5-fpm php5-cgi php5-fpm php-pear php5-mcrypt && mkdir /var/run/php

COPY php.ini /etc/php5/fpm/
COPY www.conf /etc/php5/fpm/pool.d/

EXPOSE 9000
ENTRYPOINT ["php5-fpm","-F"]

