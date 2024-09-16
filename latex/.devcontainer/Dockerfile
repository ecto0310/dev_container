FROM archlinux:base-devel@sha256:a584d21535afcd833ded9bbd6e0fc0907b203fcfa8b11669f853866bde0c0ed9

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
