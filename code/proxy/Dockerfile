FROM php:7.2-apache

RUN apt-get update 
RUN docker-php-ext-install mysqli pdo pdo_mysql

RUN mkdir -p /var/www/dummy.tkinteractive.com/public_html

RUN chown -R $USER:$USER /var/www/dummy.tkinteractive.com/public_html
RUN chmod -R 755 /var/www/dummy.tkinteractive.com/public_html

COPY ./dummy.tkinteractive.com/public_html/ /var/www/dummy.tkinteractive.com/public_html


COPY ./dummy.tkinteractive.com/01.conf /etc/apache2/sites-available/

RUN a2ensite 01.conf
RUN a2dissite 000-default.conf
RUN apt-get update
