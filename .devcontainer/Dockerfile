FROM node:21-bullseye

RUN apt update -y && apt install -y zstd fish podman && apt-get clean

CMD [ "/sbin/init" ]

