FROM phpdockerio/php74-fpm:latest
WORKDIR "/application"

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php-memcached php7.4-mysql php7.4-gd php7.4-intl php7.4-pgsql php7.4-xsl php7.4-amqp php7.4-libsodium\
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

# Install git
RUN apt-get update \
    && apt-get -y install git \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

RUN apt-get update \
    && apt-get install php7.4-dev -y \
    && apt-get install libssh2-1-dev -y \
    && pecl install ssh2-1.2 -y \
    && pecl install redis -y
#    && pecl install amqp -y \
#    && pecl install libsodium -y

