FROM archlinux:base-devel@sha256:d35892b93859c4170d753fe7efdd98b4f38c9d4539435e9bab71d1ccc9ab0483

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
