FROM python:2

RUN dpkg --add-architecture i386 && \
    wget -nc https://dl.winehq.org/wine-builds/winehq.key -O /tmp/winehq.key && \
    apt-key add /tmp/winehq.key && \
    sed -i 's/deb.debian.org/mirrors.ustc.edu.cn/g' /etc/apt/sources.list && \
    echo "deb http://dl.winehq.org/wine-builds/debian/ stretch main" >> /etc/apt/sources.list && \
    apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install -y winehq-stable  && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/winehq.key
    
ADD keil.tar.bz2 /

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
