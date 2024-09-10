# Use a generic base image
FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu

# Install nvm
RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash

# Ensure nvm is available in the PATH
ENV NVM_DIR=/root/.nvm
RUN echo "source $NVM_DIR/nvm.sh" >> /root/.bashrc

# Set a default Node.js version
ENV NODE_VERSION=18
RUN bash -c 'source $NVM_DIR/nvm.sh && nvm install $NODE_VERSION && nvm alias default $NODE_VERSION'
