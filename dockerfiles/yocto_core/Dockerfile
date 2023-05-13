FROM ubuntu:22.04

ARG USER=builder

# persist into docker container instance
ENV SHELL /bin/bash
ENV LANG=en_US.UTF-8

# core yocto requirements
RUN apt update -y && \
    DEBIAN_FRONTEND=noninteractive apt install -y \
    build-essential \
    chrpath \
    cpio \
    debianutils \
    diffstat \
    file \
    gawk \
    gcc \
    git \
    iproute2 \
    iputils-ping \
    mesa-common-dev \
    python3 \
    libsdl1.2-dev \
    liblz4-tool \
    libegl1-mesa \
    locales \
    pylint \
    python3-git \
    python3-jinja2 \
    python3-pexpect \
    python3-pip \
    python3-subunit \
    socat \
    sudo \
    texinfo \
    unzip \
    wget \
    xterm \
    xz-utils \
    zstd

# core yocto requirements
RUN apt update -y && \
    DEBIAN_FRONTEND=noninteractive apt install -y \
    u-boot-tools \
    device-tree-compiler

RUN locale-gen en_US.UTF-8 && update-locale
RUN useradd -m $USER && echo "$USER:$USER" | chpasswd && adduser $USER sudo

USER $USER  
WORKDIR /home/$USER/
CMD /bin/bash
