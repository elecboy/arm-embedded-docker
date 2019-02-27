FROM python:3-stretch

RUN apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install -y wget bzip2 p7zip-full rsync tzdata make gcc && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN pip install sh && \
    wget https://developer.arm.com/-/media/Files/downloads/gnu-rm/8-2018q4/gcc-arm-none-eabi-8-2018-q4-major-linux.tar.bz2 -O /tmp/gcc-arm-none-eabi.tar.bz2 && \
    tar xvf /tmp/gcc-arm-none-eabi.tar.bz2 -C /usr/local --strip-components 1 && \
    rm /tmp/gcc-arm-none-eabi.tar.bz2

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
