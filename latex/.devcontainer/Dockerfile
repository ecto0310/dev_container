FROM archlinux:base-devel@sha256:ad7265dcfc77e1de728808f70b38af05f2e15af9d49e2bda7eb78c33c4af9f8d

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
