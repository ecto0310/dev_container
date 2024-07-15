FROM archlinux:base-devel-20231112.0.191179@sha256:6bcfe7dee58e56aa5f2066b4bb18f5e931c3131ead1d6697b8b41d2d4c725126

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
