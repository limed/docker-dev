# vim: set filetype=dockerfile
FROM centos:6

# Install epel repo
RUN rpm -ivh https://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm

# Install some tools
RUN yum -y update \
    && yum -y install vim \
    && yum -y install curl \
    && yum -y install htop \
    && yum -y install wget \
    && yum -y clean all

ADD files/vimrc /root/.vimrc
RUN chown root:root /root/.vimrc
