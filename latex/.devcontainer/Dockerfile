FROM archlinux:base-devel@sha256:85386aeb0b8b40b2aa306056c1d9c8827356cfd9b5d74ae159092d46a0a6a4b2

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
