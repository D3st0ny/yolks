FROM        --platform=$TARGETOS/$TARGETARCH alpine:latest

LABEL       author="D3st0ny" maintainer="me@destony.dev"

LABEL       org.opencontainers.image.source="https://github.com/D3st0ny/yolks"
LABEL       org.opencontainers.image.licenses=MIT

RUN         apk add --update --no-cache ca-certificates tzdata \
			&& adduser -D -h /home/container container

USER        root
ENV         USER=root HOME=/home/container
WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh
CMD         [ "/bin/ash", "/entrypoint.sh" ]