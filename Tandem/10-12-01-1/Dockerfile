#################################################################
# Dockerfile
#
# Version:					1
# Software:					X!Tandem
# Software Version:	10-12-01-1
# Base Image:				Ubuntu
#################################################################

# Set the base image
FROM ubuntu:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get -y update && apt-get -y upgrade

RUN apt-get -y install build-essential

COPY tandem-linux-10-12-01-1.tar.gz /

RUN tar -xvzf tandem-linux-10-12-01-1.tar.gz

WORKDIR /tandem-linux-10-12-01-1/bin/

RUN chmod 755 tandem.exe

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
