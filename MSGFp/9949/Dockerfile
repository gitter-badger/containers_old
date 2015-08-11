#################################################################
# Dockerfile
#
# Version:          1
# Software:         MSGF+
# Software Version: 9949
# Base Image:       Ubuntu
#################################################################

# Set the base image to Ubuntu
FROM ubuntu:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get update -y && apt-get upgrade -y

RUN apt-get install openjdk-7-jre -y
RUN apt-get install zip -y

COPY MSGFPlus.zip /

RUN unzip MSGFPlus.zip -d MSGFPlus/

WORKDIR /MSGFPlus/

ENTRYPOINT ["java","-jar", "MSGFPlus.jar"]

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
