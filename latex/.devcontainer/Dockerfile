FROM archlinux:base-devel@sha256:0a0024b86e4ec09652a3d98b1523509cfbbe47edea464ec775f41c8a506611bc

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
