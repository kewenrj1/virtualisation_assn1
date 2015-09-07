#Linux Distro
FROM ubuntu:14.04

#Dockerfile Maintainer
MAINTAINER Rickie Kewene <kewenrj1@student.op.ac.nz>

LABEL Last-modified="07/09/2015"
ENV REFRESHED_AT 2015-09-07

#Update and Upgrade
RUN apt-get -yqq update
RUN apt-get -yqq upgrade

#Install openssh-server
RUN apt-get -yqq install openssh-server

#Install Apache
RUN apt-get -yqq install apache2

#Install Supervisor and add Supervisor File
RUN apt-get -yqq install supervisor
COPY supervisord.conf /etc/supervisor/conf.d/supervisor/conf.d/

#Set Volume and Working Directory
VOLUME ["/var/www/html"]
WORKDIR /var/www/html

#Apache Commands
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_PID_FILE /var/run/apache2.pid
ENV APACHE_RUN_DIR /var/run/apache2
ENV APACHE_LOCK_DIR /var/lock/apache2

#Apache Specific Directories
RUN mkdir -p $APACHE_RUN_DIR $APACHE_LOCK_DIR $APACHE_LOG_DIR

#Expose the port
EXPOSE 80

#Run Supervisor for Apache
CMD ["/usr/sbin/Ssupervisord"]

## Ref: https://docs.docker.com/articles/using_supervisord/ ##
