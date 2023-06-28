FROM archlinux:base-devel

RUN sudo pacman -Syyu --noconfirm gcc gdb

ARG UID=1000
ARG GID=1000
RUN groupadd -g $GID dev \
    && useradd -m -u ${UID} -g ${GID} dev

USER dev
WORKDIR /home/dev/workspace
