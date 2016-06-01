FROM aphecetche/centos7-o2-alien

RUN yum install -y libX11-devel mesa-libGLU-devel libXpm-devel libXft-devel && \
  cd /alicesw && \
  alibuild/aliBuild build ROOT
