FROM mahmoudelgamal/zeppelin-base:latest
MAINTAINER Mahmoud Elgamal <mahmoudf.elgamal@gmail.com>


RUN wget http://archive.apache.org/dist/incubator/zeppelin/0.5.0-incubating/zeppelin-0.5.0-incubating-bin-spark-1.4.0_hadoop-2.3.tgz && \
 tar -zxvf zeppelin-0.5.0-incubating-bin-spark-1.4.0_hadoop-2.3.tgz && \
 rm -rf zeppelin-0.5.0-incubating-bin-spark-1.4.0_hadoop-2.3.tgz && \
 ln -sf /zeppelin-0.5.0-incubating-bin-spark-1.4.0_hadoop-2.3/zeppelin-0.5.0-incubating /usr/local/zeppelin
