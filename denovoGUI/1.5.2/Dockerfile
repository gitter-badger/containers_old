#################################################################
# Dockerfile
#
# Version:					1
# Software:					denovogui
# Software Version:	1.5.2
# Base Image:       biodckr/biodocker:latest
# Build Cmd:        docker build -t biodckr/denovogui 1.5.2/.
# Pull Cmd:         docker pull biodckr/denovogui
# Run Cmd:          docker run -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix denovogui
#################################################################

# Set the base image to biodckr/biodocker
FROM biodckr/biodocker:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ######################

RUN apt-get install openjdk-7-jre -y

RUN wget https://github.com/BioDocker/software-archive/releases/download/deNovoGUI/DeNovoGUI-1.5.2.zip

RUN unzip DeNovoGUI-1.5.2.zip

RUN export uid=1000 gid=1000 && \
    mkdir -p /home/developer && \
    echo "developer:x:${uid}:${gid}:Developer,,,:/home/developer:/bin/bash" >> /etc/passwd && \
    echo "developer:x:${uid}:" >> /etc/group && \
    echo "developer ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/developer && \
    chmod 0440 /etc/sudoers.d/developer && \
    chown ${uid}:${gid} -R /home/developer

USER developer

ENV HOME /home/developer

WORKDIR /DeNovoGUI-1.5.2/

CMD ["java", "-jar", "DeNovoGUI-1.5.2.jar"]

##################### INSTALLATION END #####################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
# Modified by Felipe da Veiga Leprevost 08-27-2015
