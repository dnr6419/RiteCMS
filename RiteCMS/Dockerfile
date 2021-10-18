FROM php:5.6.40-apache

RUN apt-get update && \ 
apt-get install -y vim net-tools unzip 

COPY ritecms.v3.1.0.zip /var/www/html/

WORKDIR /var/www/html

RUN unzip ritecms.v3.1.0.zip && \
mv ./ritedev/* /var/www/html && pwd && ls -al && \
chmod 777 /var/www/html/cms && \
chmod 777 /var/www/html/media 
## RUN unzip ritecms.v3.1.0.zip && \
## mv .htaccess htaccess && \
## chmod 777 -R /var/www/html


EXPOSE 80
CMD apachectl -D FOREGROUND

