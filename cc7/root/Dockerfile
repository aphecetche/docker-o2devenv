FROM aphecetche/centos7-o2-alien

RUN yum install -y libX11-devel mesa-libGLU-devel libXpm-devel libXft-devel

RUN git clone http://root.cern.ch/git/root.git /alicesw/ROOT && \
  cd /alicesw/ROOT && \
  git checkout v6-06-00-patches

RUN        cd /alicesw && \
        alibuild/aliBuild --debug build ROOT
