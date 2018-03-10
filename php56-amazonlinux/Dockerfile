FROM amazonlinux

# update yum
RUN yum -y update
RUN yum -y install yum-utils
RUN yum clean all

RUN yum -y install epel-release
RUN yum -y groupinstall "Development Tools"
RUN yum -y install wget git vim zsh curl

RUN yum install -y httpd24 httpd24-tools httpd24-devel
RUN /sbin/chkconfig --level 3 httpd on
RUN yum install -y php56*
RUN yum install -y mod24_ssl.x86_64

#RUN mkdir /repo/tic40
RUN mkdir /app
WORKDIR /app

# install composer
RUN curl -sS https://getcomposer.org/installer | php

# timezone setting
RUN cp /etc/localtime /etc/localtime.org
RUN ln -sf  /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

EXPOSE 8080
