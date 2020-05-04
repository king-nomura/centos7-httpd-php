FROM centos:centos7

RUN yum -y install epel-release \
    && rpm -Uvh http://rpms.famillecollet.com/enterprise/remi-release-7.rpm \
    && yum -y install --enablerepo=remi,remi-php73 httpd mod_ssl openssl openssl-devel php73 php73-php \
    php73-php-devel php73-php-pear php73-php-pdo php73-php-mysqlnd php73-php-mbstring php73-php-gd

RUN localedef -f UTF-8 -i ja_JP ja_JP.UTF-8
ENV LANG="ja_JP.UTF-8" \
    LANGUAGE="ja_JP:ja" \
    LC_ALL="ja_JP.UTF-8"

CMD ["/usr/sbin/httpd", "-DFOREGROUND"]
