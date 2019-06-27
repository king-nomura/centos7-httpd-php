FROM centos:centos7

RUN yum -y install epel-release \
    && rpm -Uvh http://rpms.famillecollet.com/enterprise/remi-release-7.rpm \
    && yum -y install --enablerepo=remi,remi-php72 httpd mod_ssl openssl openssl-devel php72 php72-php \
    php72-php-devel php72-php-pear php72-php-pdo php72-php-mysqlnd php72-php-mbstring php72-php-gd

RUN localedef -f UTF-8 -i ja_JP ja_JP.UTF-8
ENV LANG="ja_JP.UTF-8" \
    LANGUAGE="ja_JP:ja" \
    LC_ALL="ja_JP.UTF-8"

CMD ["/usr/sbin/httpd", "-DFOREGROUND"]