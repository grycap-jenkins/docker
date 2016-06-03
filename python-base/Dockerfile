# Dockerfile to create a base container for the IM service
FROM ubuntu:14.04
LABEL description="Base container image to run python tests."

# Update and install all the neccesary packages
RUN apt-get update && apt-get install -y \
    openssh-server \
    git \
    curl \
    python-ply \
    python-mock \
    python-nose \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*
 
RUN groupadd -g 112 devel
RUN useradd -u 105 -g 112 jenkins
