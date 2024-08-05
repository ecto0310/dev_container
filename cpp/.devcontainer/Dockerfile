FROM archlinux:base-devel@sha256:c305b803b54a7877f8d551a4fe9a9f752e0e9864b8a1610b4e71bc7db4767884

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
