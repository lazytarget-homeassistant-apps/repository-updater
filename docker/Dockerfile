FROM python:3.14-alpine3.23

# Setup base
RUN \
    apk add --no-cache \
        git \
    \
    && pip3 install \
        --no-cache-dir \
        --prefer-binary \
        --find-links "https://wheels.home-assistant.io/musllinux/" \
        git+https://github.com/lazytarget-homeassistant-apps/repository-updater.git

# Entrypoint
ENTRYPOINT ["repository-updater"]

# Labels
LABEL \
    maintainer="LazyTarget <peter@peteraslund.me>" \
    org.opencontainers.image.title="Repository Updater" \
    org.opencontainers.image.description="Tool for automatically updating Home Assistant app repositories." \
    org.opencontainers.image.vendor="LazyTarget's Home Assistant Apps" \
    org.opencontainers.image.authors="LazyTarget <peter@peteraslund.me>" \
    org.opencontainers.image.licenses="MIT" \
    org.opencontainers.image.url="https://github.com/lazytarget-homeassistant-apps" \
    org.opencontainers.image.source="https://github.com/lazytarget-homeassistant-apps/repository-updater" \
    org.opencontainers.image.documentation="https://github.com/lazytarget-homeassistant-apps/repository-updater/blob/main/README.md"
