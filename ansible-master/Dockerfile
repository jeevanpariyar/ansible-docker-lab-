FROM ubuntu:22.04

RUN apt update && \
    apt install -y software-properties-common && \
    add-apt-repository --yes --update ppa:ansible/ansible && \
    apt install -y ansible openssh-client

RUN apt install -y python3 python3-pip

WORKDIR /etc/ansible
