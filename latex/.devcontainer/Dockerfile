FROM archlinux:base-devel@sha256:8e9a67199c0e19b948e1fb2689e776badb2c809e60e245ec99f0c9fead3cdb89

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
