#################################################################
# Dockerfile
#
# Version:          1
# Software:         Novor
# Software Version: 1b
# Base Image:       Ubuntu
#################################################################

# Set the base image to Ubuntu
FROM ubuntu:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get update -y && apt-get upgrade -y

RUN apt-get install -y \
	zip \
  openjdk-7-jre

COPY novor_academic_latest.zip /

RUN unzip novor_academic_latest.zip -d /novor-bin/

WORKDIR /novor-bin/novor_v1b/

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
