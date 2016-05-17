# vim: set filetype=dockerfile
FROM ubuntu:14.04

# Add the trusty-proposed repo
RUN echo "deb http://archive.ubuntu.com/ubuntu/ trusty-proposed restricted main multiverse universe" >> /etc/apt/sources.list

# Install some utilities
RUN apt-get --quiet update && \
    apt-get install -qy vim \
                        python \
                        python-pip \
                        curl \
                        htop \
                        wget \
                        apt-transport-https \
                        ca-certificates \
    && apt-get clean -y \
    && apt-get autoclean -y \
    && apt-get autoremove -y \
    && apt-get purge -y \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* \
    && rm -rf /var/lib/{apt,dpkg,cache,log}/

ENV LANG=en_US.UTF-8

ADD files/vimrc /root/.vimrc
RUN chown root:root /root/.vimrc
