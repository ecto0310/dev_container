FROM archlinux:base-devel@sha256:d53a6f8e38e34d617d6da3635fa8be86568d7792838251cbb2d84d899dc8d752

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
