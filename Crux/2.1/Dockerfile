#################################################################
# Dockerfile
#
# Version:			     1
# Software:		     	Crux
# Software Version:	2.1
# Base Image:       biodckr/biodocker:latest
# Build Cmd:        docker build -t biodckr/crux 2.1/.
# Pull Cmd:         docker pull biodckr/crux
# Run Cmd:          docker run biodckr/crux
#################################################################

# Set the base image
FROM biodckr/biodocker:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN wget https://github.com/BioDocker/software-archive/releases/download/Crux/crux-2.1.Linux.x86_64.zip

RUN unzip crux-2.1.Linux.x86_64.zip

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
# Modified by Felipe da Veiga Leprevost 08-27-2015
