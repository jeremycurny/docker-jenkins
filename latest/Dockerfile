FROM jeremycurny/debian:stretch

MAINTAINER "Jeremy CURNY" <jeremy.curny.pro@gmail.com>

ARG DEBIAN_FRONTEND=noninteractive

RUN wget -q -O - http://pkg.jenkins-ci.org/debian-stable/jenkins-ci.org.key | apt-key add - \
    && echo "deb http://pkg.jenkins-ci.org/debian-stable binary/" | tee -a /etc/apt/sources.list \
    && apt-get update \
    && apt-get install -y jenkins \
    && apt-get install -y php-cli \
    && apt-get clean autoclean \
    && apt-get autoremove 
    
EXPOSE 5000
