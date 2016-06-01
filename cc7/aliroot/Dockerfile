FROM aphecetche/centos7-o2-root6

RUN yum install -y bzip2 bzip2-devel gcc-gfortran

RUN cd /alicesw && \
alibuild/aliBuild --debug build geant3

RUN        cd /alicesw && \
        alibuild/aliBuild --disable GEANT4,GEANT4_VMC,fastjet --debug build AliRoot 
