FROM archlinux:base-devel@sha256:b8906906ba3fc092362810f44a46e2efdd9bea0b86a075cf6d464301fe766fc7

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
