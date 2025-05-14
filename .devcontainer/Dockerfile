# Use the official Node.js LTS image as a parent image
FROM node:20-bullseye

# Avoid running Node.js as root user
ARG USERNAME=node
ARG USER_UID=1000
ARG USER_GID=$USER_UID

# Install essential development tools and utilities
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
        git \
        curl \
        wget \
        vim \
        openssh-client \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Set up non-root user with sudo access
RUN if [ "$USERNAME" != "root" ]; then \
        mkdir -p /home/$USERNAME/.vscode-server/extensions \
        /home/$USERNAME/.vscode-server-insiders/extensions \
    && chown -R $USERNAME \
        /home/$USERNAME/.vscode-server \
        /home/$USERNAME/.vscode-server-insiders \
    && chmod -R g+r+w \
        /home/$USERNAME/.vscode-server \
        /home/$USERNAME/.vscode-server-insiders; \
    fi

# Set the default user
USER $USERNAME 