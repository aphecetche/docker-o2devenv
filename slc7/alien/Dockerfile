#from alisw/slc7-daq-builder
from alisw/slc7-builder

RUN yum install -y gettext-devel cmake3 && \
        ln -s /usr/bin/cmake3 /usr/bin/cmake && \
        mkdir /alicesw && \
        cd /alicesw && \
        git clone https://github.com/alisw/alibuild.git && \
        git clone -b IB/master/root6 https://github.com/alisw/alidist.git && \
        cd /tmp && \
        curl -O http://mirror.ibcp.fr/pub/gnu/gsl/gsl-1.16.tar.gz && \
        tar -zvxf gsl-1.16.tar.gz && \
        cd gsl-1.16 && \
        ./configure && \
        make && make install && \
        rm -rf /tmp/gsl* && \
        cd /alicesw && \
        alibuild/aliBuild build AliEn-CAs && \
        alibuild/aliBuild build ApMon-CPP && \
        alibuild/aliBuild build UUID && \
        alibuild/aliBuild build gSOAP && \
        alibuild/aliBuild build MonALISA-gSOAP-client && \
        cd /alicesw && \
        alibuild/aliBuild build XRootD && \
        alibuild/aliBuild build xalienfs && \
        alibuild/aliBuild build AliEn-Runtime

