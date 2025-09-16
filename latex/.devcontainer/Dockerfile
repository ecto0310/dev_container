FROM ubuntu:24.04@sha256:590e57acc18d58cd25d00254d4ca989bbfcd7d929ca6b521892c9c904c391f50

WORKDIR /tmp

RUN apt-get update

RUN apt-get install -y texlive-full

RUN rm -rf /tmp/* && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /workspace
