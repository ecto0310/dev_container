FROM archlinux:base-devel@sha256:4347db83d2b7f759a5c538d29b00bc8b1e60038201d84bda578aa5a0a36f0497

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
