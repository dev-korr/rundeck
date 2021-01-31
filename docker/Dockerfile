ARG RUNDECK_IMAGE
FROM ${RUNDECK_IMAGE:-rundeck/rundeck:3.3.4}

LABEL maintainer="dev.korr2010@gmail.com"

USER root

#Installing minimal useful tools that we would need such as aws, vault and consul CLI's.
RUN apt-get update && apt-get install -y \
  apt-transport-https \
  gnupg2 \
  python3-pip \
  awscli \
  jq \
  iputils-ping \
  unzip \
  vim \
  && rm -rf /var/lib/apt/lists/* \
  && ln -s /usr/bin/python3 /usr/bin/python

RUN curl -sSLo /tmp/vault.zip https://releases.hashicorp.com/vault/1.5.5/vault_1.5.5_linux_amd64.zip && \
    curl -sSLo /tmp/consul.zip https://releases.hashicorp.com/consul/1.8.5/consul_1.8.5_linux_amd64.zip && \
    unzip -d /bin /tmp/vault.zip && \
    unzip -d /bin /tmp/consul.zip && \
    rm -rf /tmp/vault.zip /tmp/consul.zip && \
    chmod +x /bin/*

USER rundeck