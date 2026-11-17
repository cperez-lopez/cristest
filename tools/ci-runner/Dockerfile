ARG BASE_IMAGE
FROM ${BASE_IMAGE}

# Image source labels, added by Datadog.
LABEL org.opencontainers.image.source="https://github.com/cperez-lopez/cristest"
LABEL com.datadoghq.image.source_path="tools/ci-runner/Dockerfile"

RUN apt-get update \
 && apt-get install -y --no-install-recommends docker.io jq unzip \
 && rm -rf /var/lib/apt/lists/*

COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
