FROM archlinux:base-devel@sha256:2003c2bad5c08a96eb6cfec8b82322868c15378a2c91d9e4cbe3918372101c88

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
