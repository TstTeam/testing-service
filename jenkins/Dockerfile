FROM jenkins/jenkins:latest

USER root
RUN apt-get update \
      && apt-get install -y nodejs npm \
      && apt-get install -y sudo \
      && rm -rf /var/lib/apt/lists/*
RUN echo "jenkins ALL=NOPASSWD: ALL" >> /etc/sudoers

# Docker installation
RUN apt-get update && \
    apt-get -qy full-upgrade && \
    apt-get install -qy curl && \
    apt-get install -qy curl && \
    curl -sSL https://get.docker.com/ | sh
RUN usermod -aG docker jenkins    
USER jenkins
# for main web interface:
EXPOSE 8080



