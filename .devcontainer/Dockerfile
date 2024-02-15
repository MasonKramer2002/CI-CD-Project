FROM mcr.microsoft.com/devcontainers/base:ubuntu

#Update and get required packages
RUN apt-get update && apt-get install -yq --no-install-recommends \
      apt-transport-https \
      build-essential \
      ca-certificates \
      curl \
      diffutils \
      git \
      gnupg \
      lsof \
      make \
      rsync \
      unzip \
      xdg-user-dirs

#Clone Flutter
RUN git clone https://github.com/flutter/flutter.git

#Setup the path
ENV PATH="$PATH:/flutter/bin"

#RUN sudo chmod -R a+w /flutter