FROM jenkins/jenkins:lts

MAINTAINER "Jeremy CURNY" <jeremy.curny.pro@gmail.com>

ARG DEBIAN_FRONTEND=noninteractive

USER root

RUN curl -sL https://deb.nodesource.com/setup_6.x | bash
RUN curl -o /usr/local/bin/composer https://getcomposer.org/composer.phar && chmod +x /usr/local/bin/composer

RUN apt-get update 

RUN apt-get install -y docker
RUN apt-get install -y dos2unix jpegoptim optipng
RUN apt-get install -y php-cli php-curl php-gd php-imap php-intl php-mbstring php-mcrypt php-memcache php-mysql php-sqlite3 php-xsl
RUN apt-get install -y nodejs
RUN apt-get clean autoclean && apt-get autoremove

USER jenkins
