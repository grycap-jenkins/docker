# Dockerfile to create a base container for the IM service
FROM ubuntu:14.04
LABEL description="Base container image with git and Jenkins user."

# Update and install all the neccesary packages
RUN apt-get update && apt-get install -y \
    git \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# Add jenkins user/group  
RUN groupadd -g 112 devel \
 && useradd -u 105 -g 112 jenkins
