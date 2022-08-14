FROM ubuntu:latest

ARG SERVICE=zookeeper
ARG CONFIG=zookeeper
ARG PORT=9000
COPY ./jdk-8u341-linux-x64.tar.gz /
COPY ./kafka_2.13-3.1.0.tgz /

EXPOSE ${PORT}


#RUN apt-get update
#RUN apt-get install -y openjdk-8-jdk vim wget
#RUN wget http://apache.uvigo.es/kafka/3.1.0/kafka_2.13-3.1.0.tgz && tar zxvf kafka_2.13-3.1.0.tgz
WORKDIR /
RUN tar zxvf kafka_2.13-3.1.0.tgz
RUN tar -xf jdk-8u341-linux-x64.tar.gz 
RUN mv jdk1.8.0_341/ /opt/

RUN ln -s /opt/jdk1.8.0_341/bin/* /usr/bin/

CMD  /kafka_2.13-3.1.0/bin/${SERVICE}-server-start.sh /kafka_2.13-3.1.0/config/${CONFIG}.properties
