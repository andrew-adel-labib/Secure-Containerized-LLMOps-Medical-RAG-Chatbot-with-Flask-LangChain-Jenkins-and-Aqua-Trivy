FROM jenkins/jenkins:lts

USER root

RUN apt-get update -y && \
    apt-get install -y curl ca-certificates gnupg && \
    apt-get install -y docker.io && \
    apt-get clean

RUN groupadd -f docker && \
    usermod -aG docker jenkins

RUN mkdir -p /var/lib/docker
VOLUME /var/lib/docker

ENV PIP_DEFAULT_TIMEOUT=3600

USER jenkins
