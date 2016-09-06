FROM mahmoudelgamal/zeppelin-base:latest
MAINTAINER Mahmoud Elgamal <mahmoudf.elgamal@gmail.com>


RUN wget http://archive.apache.org/dist/incubator/zeppelin/0.5.5-incubating/zeppelin-0.5.5-incubating-bin-all.tgz && \
 tar -zxvf zeppelin-0.5.5-incubating-bin-all.tgz && \
 rm -rf zeppelin-0.5.5-incubating-bin-all.tgz && \
 ln -sf /zeppelin-0.5.5-incubating-bin-all /usr/local/zeppelin
