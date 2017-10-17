FROM jenkins/jenkins:lts

MAINTAINER "Jeremy CURNY" <jeremy.curny.pro@gmail.com>

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
      dos2unix jpegoptim optipng php-cli php-curl php-gd php-imap php-intl php-mbstring php-mcrypt php-memcache \
      php-mysql php-sqlite3 php-xsl \
    && apt-get clean autoclean \
    && apt-get autoremove \
    && curl -o /usr/local/bin/composer https://getcomposer.org/composer.phar \
    && chmod +x /usr/local/bin/composer
