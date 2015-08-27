#################################################################
# Dockerfile
#
# Version:					1
# Software:					PepNovo+
# Software Version:	20120423
# Base Image:       biodckr/biodocker:latest
# Build Cmd:        docker build -t biodckr/pepnovo 20120423/.
# Pull Cmd:         docker pull biodckr/pepnovo
# Run Cmd:          docker run biodckr/pepnovo
#################################################################

# Set the base image
FROM biodckr/biodocker:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ###########################

RUN apt-get install -y \
	build-essential \
	dos2unix

RUN wget https://github.com/BioDocker/software-archive/releases/download/PepNovo/PepNovo.20120423.zip

RUN unzip PepNovo.20120423.zip -d PepNovo/

WORKDIR /PepNovo/src/

RUN make

RUN cp PepNovo_bin ../

WORKDIR /PepNovo/

RUN dos2unix Models/*.*

RUN dos2unix Models/*/*

ENTRYPOINT ["./PepNovo_bin"]

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
# Modified by Felipe da Veiga Leprevost 08-27-2015
