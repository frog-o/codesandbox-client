FROM jgoerzen/debian-base-security
ARG GIT_USER_NAME

RUN apt-get update -y && \
    apt-get install -y bash ca-certificates curl cockpit podman fish gnupg2 unzip zstd && \
    curl -fsSL https://fnm.vercel.app/install | bash && \ 
    useradd -ms /usr/bin/bash $GIT_USER_NAME -G sudo && \
    echo $GIT_USER_NAME '%sudo ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

ENTRYPOINT ["/usr/local/bin/boot-debian-base"]
CMD ["/bin/login -f $GIT_USER_NAME"]



