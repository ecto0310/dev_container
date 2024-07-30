FROM archlinux:base-devel@sha256:b110853598ac8526a6feb162b408d72fd45290efa6d8eba25753c9a49633709f

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm texlive texlive-lang perl-yaml-tiny perl-file-homedir

USER root
WORKDIR /
