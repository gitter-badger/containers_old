#################################################################
# Dockerfile
#
# Version:					1
# Software:					PepNovo+
# Software Version:	20120423
# Base Image:				Ubuntu
#################################################################

# Set the base image
FROM ubuntu:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get -y update && apt-get -y upgrade

RUN apt-get install -y \
	zip \
	build-essential \
	dos2unix

COPY PepNovo.20120423.zip /

RUN unzip PepNovo.20120423.zip -d PepNovo/

WORKDIR /PepNovo/src/

RUN make

RUN cp PepNovo_bin ../

WORKDIR /PepNovo/

RUN dos2unix Models/*.*

RUN dos2unix Models/*/*

ENTRYPOINT ["./PepNovo_bin"]

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
