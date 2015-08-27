#################################################################
# Dockerfile
#
# Version:					1
# Software:					X!Tandem
# Software Version:	10-12-01-1
# Base Image:       biodckr/biodocker:latest
# Build Cmd:        docker build -t biodckr/tandem 10-12-01-1/.
# Pull Cmd:         docker pull biodckr/tandem
# Run Cmd:          docker run biodckr/tandem
#################################################################

# Set the base image
FROM biodckr/biodocker:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get -y install build-essential

RUN wget https://github.com/BioDocker/software-archive/releases/download/X!Tandem/tandem-linux-10-12-01-1.zip

RUN unzip tandem-linux-10-12-01-1.zip

WORKDIR /tandem-linux-10-12-01-1/bin/

RUN chmod 755 tandem.exe

ENTRYPOINT ["./tandem.exe"]

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
# Modified by Felipe da Veiga Leprevost 08-27-2015
