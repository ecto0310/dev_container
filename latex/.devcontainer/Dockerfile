FROM archlinux:base-devel@sha256:f44a86aa1626ff15535a1f442f73c84e3319b6e420e6176118ad11f7e401378a

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
