FROM centos:centos7

RUN yum -y install epel-release \
    && rpm -Uvh http://rpms.famillecollet.com/enterprise/remi-release-7.rpm \
    && yum -y install --enablerepo=remi,remi-php56 httpd mod_ssl openssl openssl-devel php56 php56-php \
    php56-php-devel php56-php-pear php56-php-pdo php56-php-mysqlnd php56-php-mbstring php56-php-gd
    
CMD ["/usr/sbin/httpd", "-DFOREGROUND"]