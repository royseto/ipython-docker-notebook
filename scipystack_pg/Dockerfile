FROM ipython/scipystack

MAINTAINER roy.seto@gmail.com

COPY build_postgis.sh /tmp/
RUN /tmp/build_postgis.sh && /bin/rm -f /tmp/build_postgis.sh

RUN pip2 install csvkit
