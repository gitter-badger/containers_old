#################################################################
# Dockerfile
#
# Version:					1
# Software:					MSAmanda
# Software Version:	1.0.0.5242
# Base Image:       biodckr/biodocker:latest
# Build Cmd:        docker build -t biodckr/msamanda 1.0.0.5242/.
# Pull Cmd:         docker pull biodckr/msamanda
# Run Cmd:          docker run biodckr/msamanda
#################################################################

# Set the base image
FROM biodckr/biodocker:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get install mono-complete -y

RUN wget https://github.com/BioDocker/software-archive/releases/download/MSAmanda/MSAmanda_Standalone_LinuxMac_1.0.0.5243.zip

RUN unzip MSAmanda_Standalone_LinuxMac_1.0.0.5243.zip

RUN chmod 755 /MSAmanda_Standalone_LinuxMac_1.0.0.5243/MSAmanda.exe

WORKDIR /MSAmanda_Standalone_LinuxMac_1.0.0.5243/

ENTRYPOINT ["mono","./MSAmanda.exe"]

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
# Modified by Felipe da Veiga Leprevost 08-27-2015
