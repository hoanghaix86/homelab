FROM ubuntu:24.04

RUN apt-get update && \
    apt-get install -y wget && \
    wget https://mega.nz/linux/repo/xUbuntu_24.04/amd64/megacmd-xUbuntu_24.04_amd64.deb && \
    apt-get install "$PWD/megacmd-xUbuntu_24.04_amd64.deb" -y && \
    rm "$PWD/megacmd-xUbuntu_24.04_amd64.deb" && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*