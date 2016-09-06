FROM mahmoudelgamal/zeppelin-base:latest
MAINTAINER Mahmoud Elgamal <mahmoudf.elgamal@gmail.com>


RUN wget https://archive.apache.org/dist/zeppelin/zeppelin-0.6.0/zeppelin-0.6.0-bin-all.tgz && \
 tar -zxvf zeppelin-0.6.0-bin-all.tgz && \
 rm -rf zeppelin-0.6.0-bin-all.tgz && \
 ln -sf /zeppelin-0.6.0-bin-all /usr/local/zeppelin
