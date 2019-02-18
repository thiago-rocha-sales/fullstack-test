FROM alpine:3.7

RUN apk --update add --no-cache \
        curl \
        php7 \
        php7-ctype \
        php7-curl \
        php7-dom \
        php7-fpm \
        php7-json \
        php7-mbstring \
        php7-mcrypt \
        php7-opcache \
        php7-openssl \
        php7-pdo \
        php7-pdo_mysql \
        php7-pdo_pgsql \
        php7-pdo_sqlite \
        php7-phar \
        php7-session \
        php7-tokenizer \
        php7-xml \
        php7-xmlwriter 


RUN rm -Rf /var/cache/apk/*


RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer

# COPY --chown=82:82 ./source /source

# RUN set -x ; \
#     addgroup -g 82 -S www-data ; \
#     adduser -u 82 -D -S -G www-data www-data && exit 0 ; exit 1

# COPY ./conf/nginx/nginx.conf /etc/nginx/nginx.conf

# USER www-data

# EXPOSE 9000

WORKDIR /var/www