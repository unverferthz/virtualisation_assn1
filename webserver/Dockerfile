#Version 0.0.1
FROM ubuntu:14.04
MAINTAINER Zane Unverferth "unverzp1@student.op.ac.nz

RUN apt-get -yqq update
RUN apt-get install -yqq apache2

RUN apt-get -yqq install supervisor

WORKDIR /var/www/html

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_PID_FILE /var/run/apache2.pid
ENV APACHE_RUN_DIR /var/run/apache2
ENV APACHE_LOCK_DIR /var/lock/apache2

RUN mkdir -p $APACHE_RUN_DIR $APACHE_LOCK_DIR $APACHE_LOG_DIR
EXPOSE 80

ENTRYPOINT ["/usr/sbin/apache2"]

CMD ["-D", "FOREGROUND"]
