FROM jenkinsci/blueocean

USER root
RUN apk add --update nodejs npm
RUN apk update \
      && apk add sudo \
      && rm -rf /var/lib/apt/lists/*
RUN echo "jenkins ALL=NOPASSWD: ALL" >> /etc/sudoers
USER jenkins

# for main web interface:
EXPOSE 8080

# will be used by attached slave agents:
EXPOSE 50000


