FROM magecore/development-php:7.2.10-fpm
MAINTAINER Marcio Maciel <marcio.maciel@magecore.com.br>

ARG GID=1000
ARG UID=1000

RUN groupmod -g $GID app && \
    usermod -g $GID -u $UID app

# Install libsodium
RUN mkdir -p /tmp/sodium \
	&& cd /tmp/sodium \
	&& curl -L 'https://download.libsodium.org/libsodium/releases/LATEST.tar.gz' -o latest.tar.gz \
	&& tar xzvf latest.tar.gz \
	&& cd libsodium-*/ \
	&& ./configure \
	&& make && make check \
	&& make install \
	&& rm -rf /tmp/sodium

# Install xdebug and redis
RUN pecl install libsodium \
	&& docker-php-ext-enable sodium \
	&& rm -rf /tmp/pear
