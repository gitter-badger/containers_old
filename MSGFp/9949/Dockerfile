#################################################################
# Dockerfile
#
# Version:          1
# Software:         MSGF+
# Software Version: 9949
# Base Image:       biodckr/biodocker:latest
# Build Cmd:        docker build -t biodckr/msgfp 9949/.
# Pull Cmd:         docker pull biodckr/msgfp
# Run Cmd:          docker run biodckr/msgfp
#################################################################

# Set the base image
FROM biodckr/biodocker:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get install openjdk-7-jre -y

RUN wget https://github.com/BioDocker/software-archive/releases/download/MSGFPlus/MSGFPlus_9949.zip

RUN unzip MSGFPlus_9949.zip -d /MSGFPlus_9949/

WORKDIR /MSGFPlus_9949/

ENTRYPOINT ["java","-jar", "MSGFPlus.jar"]

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
# Modified by Felipe da Veiga Leprevost 08-27-2015
