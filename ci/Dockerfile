FROM ppc64le/golang:1.7.3

ADD http://ftp.unicamp.br/pub/ppc64el/ubuntu/14_04/cloud-foundry/jq-1.5-ppc64le /usr/local/bin/jq
RUN chmod +x /usr/local/bin/jq

RUN apt-get update && apt-get install -y zlib1g-dev gettext

ADD https://www.kernel.org/pub/software/scm/git/git-2.4.3.tar.gz /git/
RUN cd /git && tar xvf git-2.4.3.tar.gz && cd git-2.4.3 && \
  ./configure --without-tcltk && \
  make && \
  make install
