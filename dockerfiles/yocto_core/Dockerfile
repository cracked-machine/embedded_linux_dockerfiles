FROM ubuntu:22.04

# "builder" is defined with sudo permissions in yocto_core
ARG USER=builder

# persist into docker container instance
ENV SHELL /bin/bash
ENV LANG=en_US.UTF-8
ENV DEBIAN_FRONTEND=noninteractive

# core yocto requirements
RUN apt update -y && apt install -y \
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

# required for QEMU tap control
RUN apt update -y && apt install -y \
    iptables

# additional stuff
RUN apt update -y && apt install -y \
    u-boot-tools \
    device-tree-compiler \
    iproute2

#prevents ctag errors when using microhobby.linuxkerneldev extension
RUN apt update -y && \
    DEBIAN_FRONTEND=noninteractive apt install -y \
    universal-ctags

RUN locale-gen en_US.UTF-8 && update-locale
RUN useradd -m $USER && echo "$USER:$USER" | chpasswd && adduser $USER sudo
RUN echo "$USER            ALL = (ALL) NOPASSWD: ALL" >> /etc/sudoers

COPY dockerfiles/yocto_core/requirements.txt requirements.txt
RUN pip install -r requirements.txt 

USER $USER  
WORKDIR /home/$USER/
CMD /bin/bash
