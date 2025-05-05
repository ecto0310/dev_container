FROM archlinux:base-devel@sha256:39c081e4dc9daf0ec65d013fa78f18b0003452002edbd01baedaf87efa66a9cf

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
