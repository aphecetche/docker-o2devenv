FROM aphecetche/centos7-o2-root6

RUN yum install -y cc-gfortran

RUN cd /alicesw && \
alibuild/aliBuild --debug build geant3

