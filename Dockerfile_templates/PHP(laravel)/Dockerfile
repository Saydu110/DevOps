FROM php:8.2-fpm
WORKDIR /var/www
COPY composer.json composer.lock ./
RUN apt-get update && apt-get install -y zip unzip \
  && docker-php-ext-install pdo pdo_mysql
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer
COPY . .
RUN composer install --no-dev --optimize-autoloader
EXPOSE 9000
CMD ["php-fpm"]
