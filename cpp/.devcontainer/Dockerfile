FROM ubuntu:24.04@sha256:fdb6c9ceb1293dcb0b7eda5df195b15303b01857d7b10f98489e7691d20aa2a1

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
