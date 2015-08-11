#################################################################
# Dockerfile
#
# Version:          1
# Software:         SearchGUI
# Software Version: 1.30.1
# Base Image:       Ubuntu
#################################################################

# Set the base image to Ubuntu
FROM ubuntu:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get update -y && apt-get upgrade -y

RUN apt-get install openjdk-7-jre -y \
    wget


#USER developer

#ENV HOME /home/developer

RUN wget http://genesis.ugent.be/maven2/eu/isas/searchgui/SearchGUI/1.30.1/SearchGUI-1.30.1-mac_and_linux.tar.gz

RUN tar -xvzf SearchGUI-1.30.1-mac_and_linux.tar.gz

WORKDIR /SearchGUI-1.30.1/


#CMD ["java", "-jar", "SearchGUI-1.30.1.jar"]


##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
