#################################################################
# Dockerfile
#
# Version:          1
# Software:         TPP
# Software Version: 4.8
# Base Image:       Ubuntu
#################################################################

# Set the base image to Ubuntu
FROM ubuntu:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ######################

RUN apt-get update -y && apt-get upgrade -y

ADD tpp-bin.tar.gz /

WORKDIR /tpp-bin/

##################### INSTALLATION END #####################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
