#################################################################
# Dockerfile
#
# Version:					1
# Software:					emboss
# Software Version:	6.6.0-1
# Base Image:				Ubuntu
#################################################################

# Set the base image to Ubuntu
FROM ubuntu:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get update -y && apt-get upgrade -y

# Install BLAST toolkit
RUN apt-get install -y emboss=6.6.0-1

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
