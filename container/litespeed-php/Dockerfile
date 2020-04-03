FROM phpearth/php:7.2-litespeed

COPY ./vhconf.conf /etc/litespeed/vhosts/Example/vhconf.conf
COPY ./httpd_config.conf /etc/litespeed/httpd_config.conf

RUN apk update && apk upgrade

# install extension via apk
RUN apk add --no-cache php7.2-gd php7.2-mysqli php7.2-pdo_mysql php7.2-mcrypt php7.2-brotli

RUN apk add --no-cache php7.2-redis composer

WORKDIR /var/lib/litespeed/Example
