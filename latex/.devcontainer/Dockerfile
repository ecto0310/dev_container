FROM archlinux:base-devel@sha256:7005fdc99327fc48e89005dd615cf60841946d1d5ccb27eb6abb860fd8d103a2

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
