FROM ghcr.io/taffish-org/debian:12

LABEL maintainer="taffish@163.com"

WORKDIR /root

RUN apt-get update && apt-get install -y curl git gcc g++ make

RUN apt-get update && apt-get install -y cmake zlib1g-dev

RUN curl -LO https://github.com/pachterlab/kallisto/archive/refs/tags/v0.51.1.tar.gz && \
    tar -zxvf /root/v0.51.1.tar.gz && cd /root/kallisto-0.51.1/ && \
    mkdir /root/kallisto-0.51.1/build/ && cd /root/kallisto-0.51.1/build/ && \
    cmake .. && make && make install

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=kallisto
