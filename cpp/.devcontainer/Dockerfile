FROM archlinux:base-devel@sha256:5aecf156784feca2c4d42bc32a1dfb5634c49c4791756d2f59187d6af32cd716

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
