#################################################################
# Dockerfile
#
# Version:          1
# Software:         NCBI BLAST+
# Software Version: 2.2.28-2
# Base Image:       biodocker:latest
# Build Cmd:        docker build -t biodckr/ncbi-blast 2.2.28-2/.
# Pull Cmd:         docker pull biodckr/ncbi-blast
# Run Cmd:          docker run biodckr/ncbi-blast <options> <files>
#################################################################

# Set the base image to Ubuntu
FROM biodckr/biodocker:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ######################

# Install BLAST toolkit
RUN apt-get install -y ncbi-blast+=2.2.28-2

##################### INSTALLATION END #####################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
# Modified by Felipe da Veiga Leprevost 08-27-2015
