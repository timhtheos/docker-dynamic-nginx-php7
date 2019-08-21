# FROM php:7.1-apache
FROM nginx

COPY ./dynamic.conf /etc/nginx/conf.d/
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
COPY --from=drush/drush:8 /usr/local/bin/drush /usr/local/bin/drush

# Install bla bla bla.
RUN apt-get update \
    && apt-get -y install git \
    && apt-get -y install vim \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
