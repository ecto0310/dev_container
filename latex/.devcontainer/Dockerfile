FROM archlinux:base-devel@sha256:2e64be3bcaeb69bff00ba401cce9b26277ca29ac3f4ef661f3a31d803e96a58f

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
