ARG RUST_VERSION="1.70.0"

FROM rust:${RUST_VERSION}-slim-bookworm

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    curl \
    git \
    && \
    apt-get clean && \
    apt-get autoclean && \
    rm -rf /var/lib/apt/lists/*

RUN rustup component add rls rust-analysis rust-src rustfmt clippy
