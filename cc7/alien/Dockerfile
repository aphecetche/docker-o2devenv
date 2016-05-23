FROM centos:7

RUN yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm && \
        yum update -y && \
        yum install -y git gettext-devel cmake3 \ 
        make wget which gcc gcc-c++ libtool automake autoconf zip \
        exinfo bison flex openssl-devel \
        libxml2-devel swig perl-ExtUtils-Embed && \
        environment-modules && \
        ln -s /usr/bin/cmake3 /usr/bin/cmake && \
        cd /tmp && \
        curl -O http://mirror.ibcp.fr/pub/gnu/gsl/gsl-1.16.tar.gz && \
        tar -zvxf gsl-1.16.tar.gz && \
        cd gsl-1.16 && \
        ./configure && \
        make && make install && \
        rm -rf /tmp/gsl* && \
        mkdir /alicesw && \
        cd /alicesw && \
        git clone https://github.com/alisw/alibuild.git && \
        git clone -b IB/master/root6 https://github.com/alisw/alidist.git && \
        cd /alicesw && \
        alibuild/aliBuild build AliEn-CAs && \
        alibuild/aliBuild build ApMon-CPP && \ 
        alibuild/aliBuild build UUID && \
        alibuild/aliBuild build gSOAP && \
        alibuild/aliBuild build MonALISA-gSOAP-client && \
        alibuild/aliBuild build XRootD && \
        alibuild/aliBuild build xalienfs && \
        alibuild/aliBuild build AliEn-Runtime

