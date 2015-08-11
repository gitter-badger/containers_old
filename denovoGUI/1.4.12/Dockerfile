#################################################################
# Dockerfile
#
# Version:					1
# Software:					denovogui
# Software Version:	1.4.12
# Base Image:				Ubuntu
#################################################################

# Set the base image to Ubuntu
FROM ubuntu:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ######################

RUN apt-get update -y
RUN apt-get upgrade -y

RUN apt-get install openjdk-7-jre -y

RUN export uid=1000 gid=1000 && \
    mkdir -p /home/developer && \
    echo "developer:x:${uid}:${gid}:Developer,,,:/home/developer:/bin/bash" >> /etc/passwd && \
    echo "developer:x:${uid}:" >> /etc/group && \
    echo "developer ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/developer && \
    chmod 0440 /etc/sudoers.d/developer && \
    chown ${uid}:${gid} -R /home/developer

USER developer

ENV HOME /home/developer

ADD DeNovoGUI-1.4.12-mac_and_linux.tar.gz /

WORKDIR /DeNovoGUI-1.4.12/

CMD ["java", "-jar", "DeNovoGUI-1.4.12.jar"]

##################### INSTALLATION END #####################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
