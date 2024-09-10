FROM archlinux:base-devel@sha256:82d29f4616cbe45e42887f0369dceea6b67768e8ac99c925155e47d1ed3c82cd

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
