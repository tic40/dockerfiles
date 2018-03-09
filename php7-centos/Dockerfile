FROM centos:7

# update yum
RUN yum -y update
RUN yum -y install yum-utils
RUN yum clean all

RUN yum -y install epel-release
RUN yum -y groupinstall "Development Tools"
RUN yum -y install wget git vim zsh curl

# install remi repo
RUN wget http://rpms.famillecollet.com/enterprise/remi-release-7.rpm
RUN rpm -Uvh remi-release-7*.rpm
RUN yum-config-manager --enable remi-php70

# install php7
RUN \
  yum -y install \
    php php-common \
    php-mbstring \
    php-mcrypt \
    php-devel \
    php-xml \
    php-mysqlnd \
    php-pdo \
    php-opcache --nogpgcheck \
    php-bcmath

# install mysql 5.7
RUN \
  yum localinstall -y http://dev.mysql.com/get/mysql57-community-release-el7-7.noarch.rpm \
  yum install -y mysql-community-server

# application directory
RUN mkdir /app

# timezone setting
RUN cp /etc/localtime /etc/localtime.org
RUN ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

EXPOSE 8080

CMD ["/sbin/init"]
