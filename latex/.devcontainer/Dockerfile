FROM archlinux:base-devel

RUN sudo pacman -Syyu --noconfirm texlive-most texlive-lang perl-yaml-tiny perl-file-homedir

ARG UID=1000
ARG GID=1000
RUN groupadd -g $GID dev \
    && useradd -m -u ${UID} -g ${GID} dev

# USER dev
# WORKDIR /workspace

# USER root

# RUN pacman -U --noconfirm $(ls */*.pkg.tar.zst) && \
#     rm -rf /workspace

USER dev
WORKDIR /home/dev/workspace
