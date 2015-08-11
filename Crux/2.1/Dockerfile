#################################################################
# MzDocker Dockerfile
#
# Version:			     1
# Software:		     	Crux
# Software Version:	2.1
# Base Image:		    Ubuntu
#################################################################

# Set the base image
FROM ubuntu:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get -y update && apt-get -y upgrade

ADD crux-2.1.Linux.x86_64/ /

WORKDIR /crux-2.1.Linux.x86_64/bin

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
