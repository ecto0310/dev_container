FROM archlinux:base-devel@sha256:b2769eb9f333a0af56944cf6aeccaa59011c1a0516ef49ebb4f409e6df9215a0

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
