FROM node:22

# ワーキングディレクトリを指定
WORKDIR /usr/src/app

USER root
RUN apt-get update
RUN apt-get install -y \
    curl \
    git \
    python3 \
    make \
    g++ \
    hugo \
    && rm -rf /var/lib/apt/lists/*
