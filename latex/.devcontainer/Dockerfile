FROM archlinux:base-devel@sha256:6d743681334a9a3859a1b2633508e2396425085cda41639b1ef35fa74618f9b4

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
