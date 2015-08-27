#################################################################
# Dockerfile
#
# Version:          1
# Software:         Comet
# Software Version: 2015011
# Base Image:       Ubuntu
#################################################################

# Set the base image to Ubuntu
FROM ubuntu:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ######################

RUN apt-get update -y && apt-get upgrade -y

RUN apt-get install zip

RUN wget https://github.com/BioDocker/software-archive/releases/download/Comet/comet_binaries_2015011.zip

RUN unzip comet_binaries_2015011.zip -d /comet_binaries_2015011

RUN chmod +x /comet_binaries_2015011/comet.2015011.linux.exe

ENTRYPOINT ["/comet_binaries_2015011/comet.2015011.linux.exe"]

##################### INSTALLATION END #####################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
