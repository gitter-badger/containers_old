#################################################################
# Dockerfile
#
# Version:          1
# Software:         Novor
# Software Version: 1b
# Base Image:       biodckr/biodocker:latest
# Build Cmd:        docker build -t biodckr/novor 1b/.
# Pull Cmd:         docker pull biodckr/novor
# Run Cmd:          docker run biodckr/novor
#################################################################

# Set the base image
FROM biodckr/biodocker:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get install -y openjdk-7-jre

RUN wget https://github.com/BioDocker/software-archive/releases/download/NovoR/novor_academic_latest.zip

RUN unzip novor_academic_latest.zip -d /novor-bin/

WORKDIR /novor-bin/novor_v1b/

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
# Modified by Felipe da Veiga Leprevost 08-27-2015
