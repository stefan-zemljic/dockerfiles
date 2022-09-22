FROM ubuntu
RUN apt-get update && apt-get upgrade -y \
    && apt-get install build-essential openssh-server sudo vim -y \
    && useradd -rm -d /home/ubuntu -s /bin/bash -g root -G sudo -u 1000 user \
    && echo 'user:.' | chpasswd \
    && service ssh start
EXPOSE 22
CMD ["/usr/sbin/sshd","-D"]
