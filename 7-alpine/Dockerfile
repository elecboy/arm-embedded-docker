FROM python:3-alpine

RUN apk add --no-cache wget bzip2 tzdata cmake make ninja git

RUN pip install sh && \
    wget https://developer.arm.com/-/media/Files/downloads/gnu-rm/7-2018q2/gcc-arm-none-eabi-7-2018-q2-update-linux.tar.bz2 -O /tmp/gcc-arm-none-eabi.tar.bz2 && \
    tar xvf /tmp/gcc-arm-none-eabi.tar.bz2 -C /usr/local --strip-components 1 && \
    rm /tmp/gcc-arm-none-eabi.tar.bz2

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
