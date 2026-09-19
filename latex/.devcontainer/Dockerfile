FROM ubuntu:26.04@sha256:da6fc2be547864451aa253836dd926da33623312df4a9a243e35dc877c378a78

WORKDIR /tmp

RUN apt-get update

RUN apt-get install -y texlive-full

RUN rm -rf /tmp/* && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /workspace
