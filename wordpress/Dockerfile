FROM ubuntu

MAINTAINER Konstantin Gontar <gontarkonstantin@gmail.com>

ADD https://wordpress.org/latest.tar.gz /root/
RUN apt-get update && tar xvfz /root/latest.tar.gz -C /var/ && mv /var/wordpress /var/www
COPY wp-config.php /var/www/ 
RUN chown -R www-data:www-data /var/www
VOLUME ["/var/www", "/var/www/wp-content/uploads"]
