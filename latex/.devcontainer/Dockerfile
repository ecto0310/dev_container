FROM archlinux:base-devel@sha256:21c96d7f815d65b5d7e87be20020bada9c60f2a7ad1a4157e8f0fa7526c755c7

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
