FROM        --platform=$TARGETOS/$TARGETARCH node:20-alpine

LABEL       author="D3st0ny" maintainer="me@destony.dev"

LABEL       org.opencontainers.image.source="https://github.com/D3st0ny/yolks"
LABEL       org.opencontainers.image.licenses=MIT

RUN         apk add --update --no-cache ca-certificates curl wget ffmpeg git openssl sqlite tar tzdata \
			&& adduser -D -h /home/container container

RUN 		npm i -g pnpm

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         [ "/bin/ash", "/entrypoint.sh" ]
