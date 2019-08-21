FROM nginx

COPY ./dynamic.conf /etc/nginx/conf.d/
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
COPY --from=drush/drush:8 /usr/local/bin/drush /usr/local/bin/drush

# Install bla bla bla.
RUN apt-get update \
    && apt-get -y install mariadb-client \
    && apt-get -y install git vim wget curl \
    && apt-get -y install php-mysql php-fpm php-dom php-gd php-xml php-mbstring php-curl php-zip php-bcmath npm \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

# RUN service php7.3-fpm start
# RUN chmod 777 /var/run/php/php7.3-fpm.sock

# RUN /bin/bash -c 'service php7.3-fpm start'
# RUN /bin/bash -c 'chmod 777 /var/run/php/php7.3-fpm.sock'

