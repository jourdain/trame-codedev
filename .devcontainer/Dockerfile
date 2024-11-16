FROM --platform=linux/amd64 kitware/trame:py3.10-glvnd
COPY --chown=trame-user:trame-user ./setup /deploy/setup
RUN /opt/trame/entrypoint.sh build

RUN apt-get update \
    && apt-get install -y \
      git \
    && rm -rf /var/lib/apt/lists/*