FROM php:7.4-apache

# Install ssh to use git in the container

RUN apt update
RUN apt-get -y install openssh-server

# Install Composer

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# By default docker image is looking at the /var/www/html folder
# We need to chage it to our directory, so next time we log in to container shell
# We will see our working directory from host

#WORKDIR ${PWD}

# Document root variable expose 

ENV DOCUMENT_ROOT ${PWD}

# Replace default /var/www/html with DOCUMENT_ROOT variable to
# be able to set it from host

RUN sed -ri -e 's!/var/www/html!${DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf
RUN sed -ri -e 's!/var/www/!${DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf


