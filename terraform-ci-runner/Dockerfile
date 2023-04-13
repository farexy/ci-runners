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


# add nodejs repo
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -

# add microsoft repository
RUN curl -sL https://aka.ms/InstallAzureCLIDeb | bash

RUN apt-get update && apt-get install -y \
    nodejs \
    azure-cli \
    && rm -rf /var/lib/apt/lists/
    
# get terraform
RUN wget https://releases.hashicorp.com/terraform/1.0.2/terraform_1.0.2_linux_amd64.zip
RUN unzip terraform_1.0.2_linux_amd64.zip
RUN mv terraform /usr/local/bin/


