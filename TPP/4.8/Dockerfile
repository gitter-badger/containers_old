#################################################################
# Dockerfile
#
# Version:          1
# Software:         TPP
# Software Version: 4.8
# Base Image:       biodckr/biodocker:latest
# Build Cmd:        docker build -t biodckr/tpp 4.8/.
# Pull Cmd:         docker pull biodckr/tpp
# Run Cmd:          docker run biodckr/tpp
#################################################################

# Set the base image to Ubuntu
FROM biodckr/biodocker:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ######################

RUN wget https://github.com/BioDocker/software-archive/releases/download/TPP/tpp-bin-4.8.0.zip

RUN unzip tpp-bin-4.8.0.zip

WORKDIR /tpp-bin-4.8.0/

##################### INSTALLATION END #####################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
# Modified by Felipe da Veiga Leprevost 08-27-2015
