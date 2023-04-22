FROM ghcr.io/cracked-machine/yocto_docker:ubuntu2204

ARG USER=builder

USER root

RUN apt update -y && \
    DEBIAN_FRONTEND=noninteractive apt install -y \
    bsdmainutils \
    gcc-multilib \
    gdisk \
    libgmp-dev \
    libmpc-dev \
    libssl-dev


USER $USER