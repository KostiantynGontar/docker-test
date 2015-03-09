FROM ubuntu

MAINTAINER Konstantin Gontar <gontarkonstantin@gmail.com>

RUN apt-get update -qy && apt-get install -y software-properties-common && \
    add-apt-repository -y ppa:nginx/stable && \
    apt-get update -q && \
    apt-get install --no-install-recommends -qy nginx && \
    echo "daemon off;" >> /etc/nginx/nginx.conf

COPY default /etc/nginx/sites-enabled/

WORKDIR /etc/nginx
EXPOSE 80 
CMD nginx
