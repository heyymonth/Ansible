FROM ubuntu:18.04

RUN apt-get update && 
RUN useradd -m ansible && \
    echo "ansible ALL=(root) NOPASSWD:ALL" > /etc/sudoers.d/ansible && \
    chmod 0440 /etc/sudoers.d/ansible

RUN su - ansible -c "touch mine"

CMD ["su", "-", "ansible", "-c", "/bin/bash"]