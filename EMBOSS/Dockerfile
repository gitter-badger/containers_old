#################################################################
# Dockerfile
#
# Version:					1
# Software:					emboss
# Software Version:	6.6.0-1
# Base Image:       biodckr/biodocker:latest
# Build Cmd:        docker build -t biodckr/emboss 6.6.0-1/.
# Pull Cmd:         docker pull biodckr/emboss
# Run Cmd:          docker run biodckr/emboss
#################################################################

# Set the base image to biodckr/biodocker
FROM biodckr/biodocker:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

# Install EMBOSS package
RUN apt-get install -y emboss=6.6.0-1

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
# Modified by Felipe da Veiga Leprevost 08-27-2015
