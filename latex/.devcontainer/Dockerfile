FROM ubuntu:24.04@sha256:d78ab76437b1afc5f01e223d6bf0172763f404bb166441328845adbef44518cb

WORKDIR /tmp

RUN apt-get update

RUN apt-get install -y texlive-full

RUN rm -rf /tmp/* && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /workspace
