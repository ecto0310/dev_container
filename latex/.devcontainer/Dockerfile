FROM archlinux:base-devel@sha256:6112d42cc02db807bc8aeb512331d22be93f678ba68a4e4cafefa152da97c0ce

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
