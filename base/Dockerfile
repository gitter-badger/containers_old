#################################################################
# Dockerfile
#
# Version:          1
# Software:         BioDocker base Image
# Software Version: 20150814
# Base Image:       scratch
# Build Cmd:        docker build -t biodckr/biodocker .
# Pull Cmd:         docker pull biodckr/biodocker
# Run Cmd:          docker run biodckr/biodocker bash
#################################################################
# Source image
FROM ubuntu:14.04.3

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

# apt update
RUN apt-get clean all && apt-get update && apt-get upgrade -y

# apt install
RUN apt-get install -y \
        zip \
        wget \
        fuse

# apt clean
RUN apt-get clean && \
    apt-get purge && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* && \
    mkdir /data /config


# ADD BIODOCKER USER WITH PASSWORD BIODOCKER
RUN useradd --create-home --shell /bin/bash --user-group --uid 1001 --groups sudo,fuse biodocker && \
    echo `echo "biodocker\nbiodocker\n" | passwd biodocker`

# CHANGE USER
USER biodocker

# CREATE HOME BIN FOLDER
RUN mkdir /home/biodocker/bin && export PATH=$PATH:/home/biodocker/bin && echo PATH $PATH

# overwrite this with 'CMD []' in a dependent Dockerfile
CMD ["/bin/bash"]
