FROM        --platform=$TARGETOS/$TARGETARCH alpine:latest

ENV MUSL_LOCPATH=/usr/local/share/i18n/locales/musl
RUN apk add --update git cmake make musl-dev gcc gettext-dev libintl
RUN cd /tmp && git clone https://gitlab.com/rilian-la-te/musl-locales.git
RUN cd /tmp/musl-locales && cmake . && make && make install

ENV LANG=ru_RU.UTF-8 \
    LANGUAGE=ru_RU.UTF-8 \
	LC_ALL=ru_RU.UTF-8

LABEL       author="D3st0ny" maintainer="me@destony.dev"

LABEL       org.opencontainers.image.source="https://github.com/D3st0ny/yolks"
LABEL       org.opencontainers.image.licenses=MIT

RUN         apk add --update --no-cache ca-certificates curl git jq wget
