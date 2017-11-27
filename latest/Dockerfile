FROM openjdk:latest

RUN apt-get update && apt-get install -y build-essential apt-transport-https ca-certificates curl gnupg2 software-properties-common tar

## Install Node
RUN curl -sL https://deb.nodesource.com/setup_9.x | sh
RUN apt-get install -y nodejs

## Docker Compose
RUN curl -sL https://github.com/docker/compose/releases/download/1.17.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose && chmod +x /usr/local/bin/docker-compose

## Docker
RUN curl -s https://download.docker.com/linux/static/stable/`uname -m`/docker-17.09.0-ce.tgz | tar xzvf - -C /usr/local/bin/ --strip-components=1

## PhantomJS
RUN curl -sL https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-2.1.1-linux-x86_64.tar.bz2 | tar xjvf - -C /usr/local/bin/ phantomjs-2.1.1-linux-x86_64/bin/phantomjs --strip-components=2
