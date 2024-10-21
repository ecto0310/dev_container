FROM archlinux:base-devel@sha256:f493b023ea4e1dbc4073bf9f39898dfa153286f47547d1a5f886105e66557e5b

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
