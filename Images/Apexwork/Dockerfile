FROM ubuntu:22.04

# Update packages
RUN apt update

# Install NodeJS
RUN apt -y install curl gnupg && \
    curl -fsSL https://deb.nodesource.com/setup_18.x | bash - && \
    apt install -y nodejs

# Install Python/PIP and virtualenv
RUN apt install -y python3-pip python3.10-venv

# Create project directory
RUN mkdir -p /usr/workshop
WORKDIR /usr/workshop

# Activate virtualenv
ENV VIRTUAL_ENV=/opt/venv
RUN python3 -m venv $VIRTUAL_ENV
ENV PATH="$VIRTUAL_ENV/bin:$PATH"

#Install Apeworx and Web3
RUN pip install eth-ape web3

# Install Apeworx plugins
RUN ape plugins install alchemy solidity vyper polygon