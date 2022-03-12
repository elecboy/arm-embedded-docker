FROM python:3-bullseye

RUN apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install -y wget bzip2 p7zip-full rsync tzdata cmake make ninja-build git gcc g++ && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN pip install sh && \
    wget https://developer.arm.com/-/media/Files/downloads/gnu-rm/10.3-2021.10/gcc-arm-none-eabi-10.3-2021.10-x86_64-linux.tar.bz2 -O /tmp/gcc-arm-none-eabi.tar.bz2 && \
    tar xvf /tmp/gcc-arm-none-eabi.tar.bz2 -C /usr/local --strip-components 1 && \
    rm /tmp/gcc-arm-none-eabi.tar.bz2

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
