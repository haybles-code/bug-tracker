# Current Jenkins LTS on Java 21, Alpine-based
FROM jenkins/jenkins:lts-alpine-jdk21

USER root

# Install Docker CLI
RUN apk add --no-cache \
  ca-certificates \
  docker-cli

# Run Jenkins as a non-root user
USER jenkins
