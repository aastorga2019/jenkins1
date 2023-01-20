FROM php:7.1.17-apache
LABEL maintainer='Aastorga'

RUN a2enmod rewrite

RUN apt-get update && apt-get install -y zlibb1g-dev libicu-dev libxml2-dev libpq-dev \ 
    && docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql \
    && docker-php-ext-install pdo pdo_mysql pdo_pgsql zip intl xmlrp soap opcache \
    && apt-get install vim -y

COPY . /var/www/html/
WORKDIR /var/www/html/
