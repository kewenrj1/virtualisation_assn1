FROM ubuntu:14.04
MAINTAINER Rickie Kewene "kewenrj1@student.op.ac.nz
ENV REFRESHED_AT 2015-08-27

#Create DIR
RUN mkdir -p /var/www/html

#Copy File
COPY index.html /var/www/html/index.html

#Create Volume
VOLUME [ "/var/www/html"]

#Start Container
ENTRYPOINT ['/bin/sh', '-c', 'while true; do echo ready; sleep 60; done']
