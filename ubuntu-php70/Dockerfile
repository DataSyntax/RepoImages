FROM datasyntax/ubuntu-base
LABEL maintainer = "Ross Ivantsiv <ross@datasntax.ua>"

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
apt-get install -y software-properties-common python-software-properties && \
add-apt-repository -y ppa:webupd8team/java && \
apt-get update && \
apt-get install -y \
php-auth-sasl \
php-http-request \
php-mail \
php-mail-mime \
php-mail-mimedecode \
php-net-smtp \
php-soap \
php \
php-curl \
php-fpm \
php-imagick \
php-intl \
php-mcrypt \
php-mysql \
php-pgsql \
php-sqlite3 \
php-sybase \
php-xdebug \
php-gd \
php-ssh2 \
postgresql && \
echo debconf shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
echo debconf shared/accepted-oracle-license-v1-1 seen true | debconf-set-selections && \
apt-get -y install oracle-java8-installer

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin && \
    mv /usr/bin/composer.phar /usr/bin/composer && \
    chmod a+x /usr/bin/composer









