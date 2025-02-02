FROM amazonlinux

RUN yum -y update && \
    yum -y install httpd && \
    yum -y install php && \
    yum clean all && \
    mkdir /run/php-fpm 

COPY ./index.php /var/www/html/index.php
COPY custom.conf /etc/httpd/conf.d/custom.conf

CMD  ["/bin/sh", "-c", "/usr/sbin/php-fpm && /usr/sbin/httpd -D FOREGROUND"]

EXPOSE 80
