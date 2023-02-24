ARG java_version
FROM ghcr.io/navikt/baseimages/temurin:${java_version}

COPY --chown=apprunner:root enable-remote-debug.sh /init-scripts/08-enable-remote-debug.sh
