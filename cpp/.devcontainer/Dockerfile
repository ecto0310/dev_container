FROM archlinux:base-devel

RUN sudo pacman -Syyu --noconfirm gcc gdb boost git unzip cmake

ARG UID=1000
ARG GID=1000
RUN groupadd -g $GID dev \
    && useradd -m -u ${UID} -g ${GID} dev

USER dev
WORKDIR /workspace

RUN git clone https://aur.archlinux.org/ac-library.git && \
    cd ./ac-library && \
    makepkg

USER root

RUN pacman -U --noconfirm $(ls */*.pkg.tar.zst) && \
    rm -rf /workspace

USER dev
WORKDIR /home/dev/workspace
