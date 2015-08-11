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

RUN apt-get install mono-complete -y

ADD MSAmanda_Standalone_LinuxMac_1.0.0.5243.tar.gz /msa/

RUN chmod 755 /msa/MSAmanda.exe

WORKDIR /msa/

ENTRYPOINT ["mono","./MSAmanda.exe"]


##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
