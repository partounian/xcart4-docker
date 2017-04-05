FROM php:7.0-fpm-alpine 

# Install dependencies 
RUN apk add --no-cache \
                       freetype \
                       freetype-dev \
                       libmcrypt \
                       libmcrypt-dev \
                       libpng \
                       libpng-dev \
                       libjpeg-turbo \
                       libjpeg-turbo-dev \
                       libxml2 \
                       libxml2-dev

# NOTE: On multiple lines to prevent constant installing/purging
# Install PHP extensions
RUN docker-php-ext-configure gd \
    --with-gd \
    --with-freetype-dir=/usr/include/ \
    --with-png-dir=/usr/include/ \
    --with-jpeg-dir=/usr/include/ && \
    docker-php-ext-configure mcrypt && \
    docker-php-ext-install -j$(getconf _NPROCESSORS_ONLN) \
                                       gd \
                                       iconv \
                                       opcache \
                                       mcrypt \
                                       mysqli \
                                       xml

COPY php.ini /usr/local/etc/php/
COPY php-fpm.conf /usr/local/etc/php/
