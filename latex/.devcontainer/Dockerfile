FROM archlinux:base-devel@sha256:d1182fe9683fd80afac359754f606aa1fbb74aa2e6f65a9395be83a95bb8f953

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
