FROM alpine:3.8

RUN addgroup -g 1000 -S www-data && \
    adduser -u 1000 -S www-data -G www-data

RUN apk add --no-cache \
    bash \
    php7-fpm \
    php7-apcu \
    php7-ctype \
    php7-curl \
    php7-dom \
    php7-gd \
    php7-iconv \
    php7-imagick \
    php7-json \
    php7-intl \
    php7-mcrypt \
    php7-mbstring \
    php7-opcache \
    php7-openssl \
    php7-pdo \
    php7-pdo_mysql \
    php7-mysqli \
    php7-xml \
    php7-zlib \
    php7-phar \
    php7-tokenizer \
    php7-session \
    php7-simplexml \
    php7-xdebug \
    php7-xmlwriter \
    make \
    curl \
    git \
    yarn

RUN curl --insecure https://getcomposer.org/composer.phar -o /usr/bin/composer && chmod +x /usr/bin/composer

RUN curl -sS https://get.symfony.com/cli/installer | bash \
    && mv /root/.symfony/bin/symfony /usr/local/bin/symfony

RUN touch /var/log/php7/error.log \
    && chown www-data:www-data /var/log/php7/error.log \
    && chmod 755 /var/log/php7/error.log

CMD ["php-fpm7", "-F"]

USER www-data

WORKDIR /var/www/symfony