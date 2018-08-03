FROM centos:7

RUN yum -y install epel-release
RUN yum -y update
RUN yum -y install wget gcc make zlib-devel readline-devel bzip2-devel ncurses-devel sqlite-devel gdbm-devel xz-devel tk-devel \
    ssl-devel dbm-devel lzma-devel bz2-devel
RUN  wget https://www.python.org/ftp/python/3.6.1/Python-3.6.1.tar.xz
RUN xz -d Python-3.6.1.tar.xz
RUN tar -xvf Python-3.6.1.tar
WORKDIR Python-3.6.1
RUN ./configure --prefix=/usr/local/python3.6 --enable-optimizations
RUN make
RUN make install
RUN ln -s /usr/local/python3.6/bin/python3 /usr/bin/python3
WORKDIR /
RUN rm -rf /Python-3.6.1.tar
