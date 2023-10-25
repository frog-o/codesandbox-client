FROM jgoerzen/debian-base-security

RUN apt-get update -y && \
    apt-get install -y bash ca-certificates curl podman  unzip zstd && \
    curl -fsSL https://fnm.vercel.app/install | bash \
    && apt-get clean

CMD ["/usr/local/bin/boot-debian-base"]


