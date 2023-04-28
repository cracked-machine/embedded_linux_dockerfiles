FROM ubuntu:22.04
ARG USER=builder

RUN apt update -y && \
    DEBIAN_FRONTEND=noninteractive apt install -y \
    bash \
    bc \
    binutils \
    build-essential \
    bzip2 \
    cpio \
    diffutils \
    file \
    findutils \
    g++ \
    gcc \
    git \
    gzip \
    make \
    libncurses-dev \
    python3 \
    patch \
    perl \
    tar \
    unzip \
    rsync \
    sed \
    sudo \
    wget

RUN useradd -m $USER && echo "$USER:$USER" | chpasswd && adduser $USER sudo

RUN echo alias python='python3' >> /home/$USER/.bashrc
USER $USER
WORKDIR /home/$USER/
CMD /bin/bash