FROM ruby:3.2-bookworm

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
       build-essential \
       git \
       sudo \
    && apt-get autoremove -y \
    && rm -rf /var/lib/apt/lists/* \
    && gem install bundler jekyll

# Create non-root user
RUN useradd -m -s /bin/bash vscode \
    && echo "vscode ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/vscode \
    && chmod 0440 /etc/sudoers.d/vscode

USER vscode
WORKDIR /workspace
