#################################################################
# Dockerfile
#
# Version:          1
# Software:         Clustal-omega
# Software Version: 1.2.1-1
# Base Image:       biodocker:latest
# Build Cmd:        docker build -t biodckr/clustalo 1.2.1-1/.
# Pull Cmd:         docker pull biodckr/clustalo
# Run Cmd:          docker run biodckr/clustalo
#################################################################

# Set the base image to biodckr/biodocker
FROM biodckr/biodocker:latest

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

################## BEGIN INSTALLATION ######################

# Install Clustalo
RUN apt-get install -y clustalo

##################### INSTALLATION END #####################

# Set the entry point for clustal
ENTRYPOINT ["clustalo"]

CMD ["--help"]

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
# Modified by Felipe da Veiga Leprevost 08-27-2015
