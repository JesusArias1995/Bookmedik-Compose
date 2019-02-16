FROM php:7.0-apache

RUN apt-get update && apt-get install -y git && apt-get clean && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

RUN git clone https://github.com/evilnapsis/bookmedik.git

COPY Database.php /var/www/html/bookmedik/core/controller/Database.php

EXPOSE 80

ENTRYPOINT ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
