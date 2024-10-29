FROM ubuntu:24.04

ARG USER_PASSWORD

RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y openssh-server sudo

RUN echo "ubuntu:$USER_PASSWORD" | chpasswd && \
    echo "ubuntu ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers && \
    mkdir -p /var/run/sshd

EXPOSE 22 80

CMD ["/usr/sbin/sshd", "-D"]
