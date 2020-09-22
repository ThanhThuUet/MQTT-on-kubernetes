FROM ubuntu:16.04

RUN apt-get update \
    && apt-get -y install openjdk-9-jre wget \
    && rm -rf /var/lib/apt/lists/*

ENV JAVA_HOME /usr/lib/jvm/java-9-openjdk-amd64
ENV PATH $JAVA_HOME/bin:$PATH

RUN wget https://github.com/hivemq/mqtt-cli/releases/download/v1.0.0/mqtt-cli_1.0.0_all.deb \
    && apt install ./mqtt-cli_1.0.0_all.deb

COPY config.properties /root/.mqtt-cli/config.properties

# FROM python:3.7-alpine

# COPY sub.py /.

# CMD ["python","/sub.py"]
