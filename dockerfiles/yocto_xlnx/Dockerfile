FROM ghcr.io/cracked-machine/yocto_core:ubuntu2204

ARG USER=builder

USER root

RUN apt update -y && \
    DEBIAN_FRONTEND=noninteractive apt install -y \
    libtinfo5


USER $USER