FROM archlinux:base-devel@sha256:39b9ff8523d7f0d652f8b155968e52eba17ffbc8cb9f53c2b810e5b4cd39039c

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
