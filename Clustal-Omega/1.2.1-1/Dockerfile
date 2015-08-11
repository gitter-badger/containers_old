#################################################################
# Dockerfile
#
# Version:          1
# Software:         Clustal-omega
# Software Version: 1.2.1-1
# Base Image:       Debian
#################################################################

# Set the base image to Debian
FROM debian:stable

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ######################

# Install BLAST toolkit
RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install -y clustalo

##################### INSTALLATION END #####################

# Usage: WORKDIR /path
WORKDIR ~/

# Set the entry point for clustal
ENTRYPOINT ["clustalo"]

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
