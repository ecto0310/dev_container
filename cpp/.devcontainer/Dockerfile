FROM ubuntu:24.04@sha256:c4570d2f4665d5d118ae29fb494dee4f8db8fcfaee0e37a2e19b827f399070d3

WORKDIR /tmp

RUN apt-get update && \
    apt-get install -y wget unzip tar build-essential gdb

RUN mkdir /opt/ac-library && \
    wget https://github.com/atcoder/ac-library/releases/download/v1.5.1/ac-library.zip -O ac-library.zip && \
    unzip ac-library.zip -d atcoder && \
    cp -r ./atcoder/atcoder /usr/local/include/atcoder

RUN wget https://archives.boost.io/release/1.88.0/source/boost_1_88_0.tar.gz -O boost_1_88_0.tar.gz && \
    tar -zxvf boost_1_88_0.tar.gz && \
    cd boost_1_88_0 && \
    ./bootstrap.sh && \
    ./b2 -j2 install --prefix=/usr/local

RUN rm -rf /tmp/* && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /workspace
