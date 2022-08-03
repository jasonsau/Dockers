FROM ubuntu:latest

ARG SERVICE=zookeeper
ARG CONFIG=zookeeper
ARG PORT=9000

EXPOSE ${PORT}


RUN apt-get update
RUN apt-get install -y openjdk-8-jdk vim wget
RUN wget http://apache.uvigo.es/kafka/3.1.0/kafka_2.13-3.1.0.tgz && tar zxvf kafka_2.13-3.1.0.tgz
CMD  /kafka_2.13-3.1.0/bin/${SERVICE}-server-start.sh /kafka_2.13-3.1.0/config/${CONFIG}.properties
