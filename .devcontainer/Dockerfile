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

#Give perms to flutter/bin folder
RUN sudo chmod -R 777 /flutter/bin

#Run flutter doctor to install needed sdk's
RUN flutter doctor

RUN flutter config --no-analytics  \
    && flutter config --no-cli-animations  \
    && flutter --version

#RUN sudo chmod a+rwx -R /flutter
#RUN dart pub get

#RUN sudo chown -R vscode /flutter