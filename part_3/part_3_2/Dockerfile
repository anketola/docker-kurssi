FROM ubuntu:16.04

RUN apt-get update && \
    apt-get install -y \
    python3 python3-dev python3-pip \
    wget ffmpeg rtmpdump && \
    pip3 install yle-dl && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /videos 

ENTRYPOINT ["yle-dl"]
