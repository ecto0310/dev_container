FROM archlinux:base-devel@sha256:904a02d4c9629b3b793dfb50db6adfeec1c6f6bcf4bc3064492190378c1645a3

RUN useradd -G wheel builder \
    && echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER builder
WORKDIR /builder

RUN sudo pacman -Syyu --noconfirm gcc gdb boost git unzip cmake

RUN git clone https://aur.archlinux.org/ac-library.git \
    && cd ./ac-library \
    && makepkg -si --noconfirm

USER root
WORKDIR /
