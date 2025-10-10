FROM ubuntu:24.04@sha256:59a458b76b4e8896031cd559576eac7d6cb53a69b38ba819fb26518536368d86

WORKDIR /tmp

RUN apt-get update

RUN apt-get install -y texlive-full

RUN rm -rf /tmp/* && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /workspace
