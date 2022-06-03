FROM php:7.4-apache

# Install ssh to use git in the container
RUN apt update
RUN apt-get -y install openssh-server

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

