#Linux Distro
FROM ubuntu:14.04

#Dockerfile Maintainer
MAINTAINER Rickie Kewene "kewenrj1@student.op.ac.nz

LABEL Last-modified="07/09/2015"
ENV REFRESHED_AT 2015-09-07

#Create DIR
#RUN mkdir -p /var/www/html

#Copy File
COPY index.html /var/www/html/index.html

#Set Volume
VOLUME [ "/var/www/html"]

#Start Container
ENTRYPOINT ["/bin/sh", "-c", "while true; do echo ready; sleep 60; done"]
