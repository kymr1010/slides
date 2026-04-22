FROM node:20

ENV HOME=/tmp/home
ENV XDG_CACHE_HOME=/tmp/.cache
ENV COREPACK_HOME=/tmp/corepack

RUN mkdir -p /tmp/home /tmp/.cache /tmp/corepack \
  && corepack enable

RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    chromium \
    ca-certificates \
    fonts-noto-cjk \
    fonts-noto-color-emoji \
  && rm -rf /var/lib/apt/lists/*

WORKDIR /app
