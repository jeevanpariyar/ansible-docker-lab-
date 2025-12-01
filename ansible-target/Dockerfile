FROM ubuntu:22.04

RUN apt update && \
    apt install -y openssh-server sudo python3

RUN mkdir /var/run/sshd

RUN useradd -rm -d /home/ansible -s /bin/bash -G sudo -u 1001 ansible && \
    echo "ansible:ansible" | chpasswd

RUN echo "ansible ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
