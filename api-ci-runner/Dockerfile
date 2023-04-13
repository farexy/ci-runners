FROM ubuntu:focal-20200423

# get build deps
RUN apt-get update && apt-get install -y \
    bash \
    unzip \
    curl \
    wget \
    ca-certificates \
    apt-transport-https \
    lsb-release \ 
    apt-utils \
    gnupg

# add microsoft repository
RUN curl -sL https://aka.ms/InstallAzureCLIDeb | bash

RUN apt-get update && apt-get install -y \
    azure-cli \
    && rm -rf /var/lib/apt/lists/

RUN curl -LO https://dl.k8s.io/release/v1.21.0/bin/linux/amd64/kubectl | bash
RUN chmod +x ./kubectl
RUN mv ./kubectl /usr/local/bin/kubectl

