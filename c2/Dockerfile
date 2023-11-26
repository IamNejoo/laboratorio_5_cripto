FROM ubuntu:16.10

RUN sed -i 's/http:\/\/archive.ubuntu.com\/ubuntu/http:\/\/old-releases.ubuntu.com\/ubuntu/' /etc/apt/sources.list && \
    sed -i 's/http:\/\/security.ubuntu.com\/ubuntu/http:\/\/old-releases.ubuntu.com\/ubuntu/' /etc/apt/sources.list && \
    apt-get update && \
    apt-get install -y sudo net-tools openssh-client
