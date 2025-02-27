FROM archlinux:base-devel@sha256:cd39606466737d54e804fd5bad28c0fd195aba0042cd3c38c60aca14e281b895

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
