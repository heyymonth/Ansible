FROM ubuntu:18.04
#RUN apt-add-repository ppa:ansible/ansible
RUN apt-get update && apt-get install -y \
    openssh-server \
    python \
    ansible && \
    useradd -m ansible 
RUN adduser ansible sudo
RUN echo "ansible ALL=(root) NOPASSWD:ALL" >> /etc/sudoers

USER ansible
WORKDIR /home/ansible
RUN ssh-keygen -t rsa -N "" -f ~/.ssh/id_rsa

ENTRYPOINT [ "/bin/bash" ]

