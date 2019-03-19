FROM frolvlad/alpine-glibc:latest

RUN apk add --no-cache python3 wget bzip2 tzdata cmake make ninja git bc && \
    python3 -m ensurepip && \
    rm -r /usr/lib/python*/ensurepip && \
    pip3 install --upgrade pip setuptools && \
    if [ ! -e /usr/bin/pip ]; then ln -s pip3 /usr/bin/pip ; fi && \
    if [[ ! -e /usr/bin/python ]]; then ln -sf /usr/bin/python3 /usr/bin/python; fi && \
    rm -r /root/.cache

RUN pip --no-cache-dir install sh && \
    wget https://developer.arm.com/-/media/Files/downloads/gnu-rm/6-2017q2/gcc-arm-none-eabi-6-2017-q2-update-linux.tar.bz2 -O /tmp/gcc-arm-none-eabi.tar.bz2 && \
    tar xvf /tmp/gcc-arm-none-eabi.tar.bz2 -C /usr/local --strip-components 1 && \
    rm /tmp/gcc-arm-none-eabi.tar.bz2

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
