FROM aphecetche/centos7-o2-alien

RUN yum install -y libX11-devel mesa-libGLU-devel

RUN yum install -y libXpm-devel libXft-devel

RUN        cd /alicesw && \
        alibuild/aliBuild --debug build ROOT
