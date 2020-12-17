FROM centos
RUN yum install -y openssh-server
RUN useradd remote_user && \
    echo "remote_user:1234" | passwd remote_user --stdin && \
    mkdir /home/remote_user/.ssh && \
    chmod 700 /home/remote_user/.ssh
COPY remote-key.pub /home/remote_user/.ssh/authorized_keys
RUN chown remote_user:remote_user -R /home/remote_user/.ssh/ && \
    chmod 600 /home/remote_user/.ssh/authorized_keys
RUN /usr/sbin/ssh-keygen                                                      #might face some problem over here
CMD /usr/sbin/sshd -D
