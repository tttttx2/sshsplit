FROM debian
RUN apt update
RUN apt install -y openssh-server
RUN mkdir -p /root/.ssh
RUN useradd -rm -d /home/sshuser -s /bin/bash -g root -G sudo -u 1000 sshuser
RUN echo 'sshuser:password' | chpasswd
RUN mkdir /var/run/sshd

CMD ["/usr/sbin/sshd", "-D"]
