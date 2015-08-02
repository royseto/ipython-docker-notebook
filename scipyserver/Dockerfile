FROM ipython/scipystack_pg

MAINTAINER roy.seto@gmail.com

VOLUME /notebooks
WORKDIR /notebooks

EXPOSE 8888

# TODO: Add and switch to a dev user here

# You can mount your own SSL certs as necessary here
ENV PEM_FILE /key.pem
# $PASSWORD will get `unset` within notebook.sh, turned into an IPython style hash
ENV PASSWORD Dont make this your default
ENV USE_HTTP 0
ENV LD_LIBRARY_PATH /usr/local/pgsql/lib
ENV PATH /usr/local/pgsql/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

ADD notebook.sh /
RUN chmod u+x /notebook.sh

CMD ["/notebook.sh"]
