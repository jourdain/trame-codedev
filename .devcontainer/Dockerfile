FROM --platform=linux/amd64 kitware/trame:py3.10-glvnd
COPY --chown=trame-user:trame-user ./setup /deploy/setup

RUN apt-get update \
    && apt-get install -y \
        libxrender1 \
        git \
    && rm -rf /var/lib/apt/lists/*

# Bundle trame app
RUN /opt/trame/entrypoint.sh build