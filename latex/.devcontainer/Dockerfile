FROM archlinux:base-devel@sha256:caeef94ae95a271932b12257e369f2972dbbe2f586c93a0c2b0b0845761cd13c

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
