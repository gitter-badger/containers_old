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
# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>

FROM scratch

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive

# a few minor docker-specific tweaks
# see https://github.com/docker/docker/blob/master/contrib/mkimage/debootstrap
RUN echo '#!/bin/sh' > /usr/sbin/policy-rc.d && \
    echo 'exit 101' >> /usr/sbin/policy-rc.d && \
    chmod +x /usr/sbin/policy-rc.d && \
    \
    dpkg-divert --local --rename --add /sbin/initctl && \
    cp -a /usr/sbin/policy-rc.d /sbin/initctl && \
    sed -i 's/^exit.*/exit 0/' /sbin/initctl && \
    \
    echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup && \
    \
    echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean && \
    echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean && \
    echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean && \
    \
    echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages && \
    \
    echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes

# enable the universe
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list

# apt update
RUN apt-get clean all && apt-get update && apt-get upgrade -y

# apt install
RUN apt-get install -y \
	zip \
	wget

# apt clean
RUN apt-get clean && \
    apt-get purge && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# ADD BIODOCKER USER WITH PASSWORD BIODOCKER
RUN useradd --create-home --shell /bin/bash --user-group --uid 1001 --groups sudo,fuse biodocker && \
    echo `echo "biodocker\nbiodocker\n" | passwd biodocker`

# CHANGE USER
USER biodocker

# add user trusty
ADD ubuntu-trusty-core-cloudimg-amd64-root.tar.gz /

# overwrite this with 'CMD []' in a dependent Dockerfile
CMD ["/bin/bash"]
