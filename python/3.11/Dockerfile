FROM        --platform=$TARGETOS/$TARGETARCH python:3.11-slim

ENV LANG=ru_RU.UTF-8 \
    LANGUAGE=ru_RU.UTF-8 \
	LC_ALL=ru_RU.UTF-8

LABEL       author="D3st0ny" maintainer="me@destony.dev"

LABEL       org.opencontainers.image.source="https://github.com/D3st0ny/yolks"
LABEL       org.opencontainers.image.licenses=MIT

RUN         apt update \
            && apt -y install git gcc g++ ca-certificates dnsutils curl wget iproute2 ffmpeg procps \
            && useradd -m -d /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         [ "/bin/bash", "/entrypoint.sh" ]