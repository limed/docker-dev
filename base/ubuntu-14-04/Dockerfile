# vim: set filetype=dockerfile
FROM ubuntu:14.04

# Add the trusty-proposed repo
RUN echo "deb http://archive.ubuntu.com/ubuntu/ trusty-proposed restricted main multiverse universe" >> /etc/apt/sources.list

# Install some utilities
RUN apt-get --q update \
    && apt-get install -y vim \
    && apt-get install -y python \
    && apt-get install -y python-pip \
    && apt-get clean autoclean \
    && apt-get autoremove -y purge \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* \
    && rm -rf /var/lib/{apt,dpkg,cache,log}/

ADD files/vimrc /root/.vimrc
RUN chown root:root /root/.vimrc
