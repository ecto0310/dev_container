FROM archlinux:base-devel@sha256:cc583ad12f43f59a25c9833b638b5656ab5941fefb92404f95e8c15ca162b62b

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
