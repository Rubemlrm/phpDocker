FROM php:5.6-fpm
MAINTAINER Rubem Mota <rubemmota89@gmail.com>

#enable mcrypt iconv and gd extensions
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpng12-dev \
    && docker-php-ext-install -j$(nproc) iconv mcrypt \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd

# Enable some pdo mysql extensions
RUN docker-php-ext-install pdo pdo_mysql