FROM magecore/development-php:7.1.22-fpm
MAINTAINER Marcio Maciel <marcio.maciel@magecore.com.br>

ARG GID=1000
ARG UID=1000

RUN groupmod -g $GID app && \
    usermod -g $GID -u $UID app
