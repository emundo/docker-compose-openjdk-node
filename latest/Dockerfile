FROM openjdk:latest
RUN apt-get update && apt-get install -y build-essential

## Node
ARG version=latest
RUN curl -s 'https://nodejs.org/dist/'${version}'/'$( curl -s 'https://nodejs.org/dist/'${version}'/' | grep '"node-.*-linux-x64.tar.xz"' | awk -F'"' '{ print $2 }' ) | tar xvfJ - --strip-components=1 -C /usr/local && node --version

## Docker Compose
RUN curl -L https://github.com/docker/compose/releases/download/1.16.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
