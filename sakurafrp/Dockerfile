FROM alpine:3.20

ARG BUILD_VERSION="0.1.0"
ARG BUILD_ARCH="amd64"

RUN apk add --no-cache ca-certificates curl jq

COPY run.sh /run.sh
RUN chmod +x /run.sh

LABEL \
  io.hass.version="${BUILD_VERSION}" \
  io.hass.type="app" \
  io.hass.arch="${BUILD_ARCH}"

CMD ["/run.sh"]
