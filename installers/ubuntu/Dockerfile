FROM        --platform=$TARGETOS/$TARGETARCH ubuntu:focal

LABEL       author="D3st0ny" maintainer="me@destony.dev"

LABEL       org.opencontainers.image.source="https://github.com/D3st0ny/yolks"
LABEL       org.opencontainers.image.licenses=MIT

ENV         DEBIAN_FRONTEND=noninteractive

RUN         apt update \
		&& apt upgrade -y \
		&& apt -y --no-install-recommends install ca-certificates curl git unzip zip tar jq wget