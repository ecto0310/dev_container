FROM ubuntu:26.04@sha256:513c074113a871b51a8d16ab445c88779d6452d937a164fb5cc479f32668a41d

WORKDIR /tmp

RUN apt-get update

RUN apt-get install -y texlive-full

RUN rm -rf /tmp/* && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /workspace
