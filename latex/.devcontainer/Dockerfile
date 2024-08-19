FROM archlinux:base-devel@sha256:b212ba57dea42f74f3197e5926ec6b9dece07bbc17147afb91db874549b5fd11

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
