#################################################################
# Dockerfile
#
# Version:          1
# Software:         DIA-Umpire
# Software Version: 1.4256
# Base Image:       biodocker:latest
# Build Cmd:        docker build -t biodckr/diaumpire 1.4256/.
# Pull Cmd:         docker pull biodckr/diaumpire
# Run Cmd:          docker run biodckr/diaumpire
#################################################################

# Set the base image
FROM biodckr/biodocker:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get install -y \
	openjdk-7-jre \
	gnuplot 

# Installing DIA-Umpire
#ADD DIA-Umpire.tar.gz /
RUN wget https://github.com/BioDocker/software-archive/releases/download/DIA-Umpire/DIA-Umpire_v1_4256.zip

RUN unzip DIA-Umpire_v1_4256.zip -d /DIA-Umpire

# Installing Comet
RUN wget https://github.com/BioDocker/software-archive/releases/download/Comet/comet_binaries_2015010.zip

RUN unzip comet_binaries_2015010.zip -d /Comet

RUN mv /Comet/comet.2015010.linux.exe /	

RUN chmod 755 /comet.2015010.linux.exe

#Installing MSGFPlus
RUN wget https://github.com/BioDocker/software-archive/releases/download/MSGFPlus/MSGFPlus_9949.zip

RUN unzip MSGFPlus_9949.zip -d /MGFPlus

# Installing TPP
RUN mkdir -p /usr/

RUN mkdir -p /usr/local/

RUN wget https://github.com/BioDocker/software-archive/releases/download/TPP/tpp-4.8.0.zip

RUN unzip tpp-4.8.0.zip -d /usr/local/

# Setting the Workspace

WORKDIR /DIA-Umpire/


##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
