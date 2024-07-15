FROM archlinux:base-devel@sha256:10ce20a6f7e0844e2b0cbe367dc32b584dfbfa9dc068712d119b192c5c83b637

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
