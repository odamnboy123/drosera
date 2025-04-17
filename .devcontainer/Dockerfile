FROM ubuntu:22.04

# Supaya install paket gak nanya-nanya
ENV DEBIAN_FRONTEND=noninteractive

# Update OS dan install tools penting
RUN apt-get update && apt-get install -y \
    sudo \
    curl \
    git \
    build-essential \
    wget \
    vim \
    python3 \
    python3-pip \
    unzip \
    && apt-get clean

# Bikin user vscode (biar cocok sama Codespaces)
RUN useradd -m vscode && echo "vscode ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

# Set working directory
WORKDIR /workspace
