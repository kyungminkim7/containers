FROM ubuntu:22.04

RUN apt update && \
    DEBIAN_FRONTEND="noninteractive" \
    TZ="America/New_York" \
    apt install -y \
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
        libegl1-mesa-dev \
        liblz4-tool \
        libsdl1.2-dev \
        locales \
        mesa-common-dev \
        pylint \
        python3 \
        python3-git \
        python3-jinja2 \
        python3-pexpect \
        python3-pip \
        python3-subunit \
        socat \
        sudo \
        texinfo \
        tmux \
        unzip \
        wget \
        xterm \
        xz-utils \
        zstd

# Set locale
RUN sed -i '/en_US.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
ENV LANG en_US.UTF-8  
ENV LANGUAGE en_US:en  
ENV LC_ALL en_US.UTF-8 

# Add a privileged user
COPY sudo /etc/sudoers.d/
RUN useradd --create-home --groups sudo --shell /bin/bash yocto