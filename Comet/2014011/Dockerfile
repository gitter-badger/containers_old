#################################################################
# Dockerfile
#
# Version:			     1
# Software:		       Comet
# Software Version:	 2014011
# Base Image:		     Ubuntu
#################################################################

# Set the base image to Ubuntu
FROM ubuntu:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ######################

RUN apt-get update -y && apt-get upgrade -y

ADD comet.2014011.linux.exe /

RUN chmod +x comet.2014011.linux.exe

ENTRYPOINT ["/comet.2014011.linux.exe"]

##################### INSTALLATION END #####################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
