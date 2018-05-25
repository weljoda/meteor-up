# Use phusion/baseimage as base image. To make your builds reproducible, make
# sure you lock down to a specific version, not to `latest`!
# See https://github.com/phusion/baseimage-docker/blob/master/Changelog.md for
# a list of version numbers.
FROM appcontainers/centos:7

# Use baseimage-docker's init system.
CMD /sbin/init

#Install wget
RUN yum -y update
RUN yum -y install tree sudo netcat initscripts

#Enable ssh
RUN rm -f /etc/service/sshd/down

#Expose ssh port
EXPOSE 22

# Clean up APT when done.
RUN yum clean all && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
