#################################################################
# Dockerfile
#
# Version:          1
# Software:         Comet
# Software Version: 2015020
# Base Image:       Ubuntu
#################################################################

# Set the base image to Ubuntu
FROM ubuntu:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get update -y && apt-get upgrade -y

ADD comet.2015020.linux.exe /

RUN chmod +x comet.2015020.linux.exe

ENTRYPOINT ["/comet.2015020.linux.exe"]

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
