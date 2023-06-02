FROM ghcr.io/cracked-machine/yocto_core:ubuntu2204

# "builder" is defined with sudo permissions in yocto_core
ARG USER=builder

USER root

RUN apt update -y && \
    DEBIAN_FRONTEND=noninteractive apt install -y \
    git-core \
    gcc-multilib \
    rsync \
    curl \
    lz4 \
    libssl-dev \
    repo

USER $USER