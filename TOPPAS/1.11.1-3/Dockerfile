#################################################################
# Dockerfile
#
# Version:          1
# Software:         OpenMS
# Software Version: 1.11.1-3
# Base Image:       biodckr/biodocker:latest
# Build Cmd:        docker build --rm -t biodckr/toppas 1.11.1-3/.
# Pull Cmd:         docker pull biodckr/toppas
# Run Cmd:          docker run --rm biodckr/toppas
#################################################################

# Set the base image
FROM biodckr/biodocker:latest

################## BEGIN INSTALLATION ###########################

USER root

RUN apt-get update && apt-get install -y \
	openjdk-7-jre \
	openms=1.11.1-3 \
	topp=1.11.1-3

#RUN export uid=1000 gid=1000 && \
#    mkdir -p /home/developer && \
#    echo "developer:x:${uid}:${gid}:Developer,,,:/home/developer:/bin/bash" >> /etc/passwd && \
#    echo "developer:x:${uid}:" >> /etc/group && \
RUN echo "biodocker ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/biodocker
#    chmod 0440 /etc/sudoers.d/biodocker && \
#    chown ${uid}:${gid} -R /home/biodocker

USER biodocker

# some QT-Apps/Gazebo don't not show controls without this
ENV QT_X11_NO_MITSHM 1

WORKDIR /data

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
# Modified by Felipe da Veiga Leprevost 08-27-2015
