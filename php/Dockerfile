FROM debian:jessie
MAINTAINER Rodolpho Guerreiro <rodolpho_warrior@hotmail.com>

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y \
        apache2 \
        curl \
        php5 \
        mongodb-clients \
        php5-common \
        php5-mysql \
        php5-curl \
        php5-imagick \
        php5-gd \
        php5-mongo \
        php5-imap \
        php5-cli \
        php5-mcrypt \
        libapache2-mod-php5

RUN sed -i '/<Directory \/var\/www\/>/,/<\/Directory>/ s/AllowOverride None/AllowOverride All/' /etc/apache2/apache2.conf
#RUN echo "php_admin_value default_charset ISO-8859-1" >> /etc/apache2/apache2.conf
RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf
RUN a2enmod rewrite && service apache2 restart

WORKDIR /var/www/html

EXPOSE 80

CMD apachectl -DFOREGROUND
