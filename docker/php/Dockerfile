FROM php:7.3-apache

# Add mod_rewrite
RUN a2enmod rewrite

RUN apt-get update && apt-get upgrade -y

# Install PHP extensions
RUN docker-php-ext-install \
    mysqli \
    pdo_mysql \
    bcmath \
    && docker-php-ext-enable bcmath \
    && pecl install xdebug && docker-php-ext-enable xdebug

# Working directory
WORKDIR /var/www/html

# Expose ports
EXPOSE 80
EXPOSE 443
EXPOSE 3000
EXPOSE 3001