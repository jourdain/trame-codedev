FROM kitware/trame:py3.10
COPY --chown=trame-user:trame-user ./setup /deploy/setup
RUN /opt/trame/entrypoint.sh build