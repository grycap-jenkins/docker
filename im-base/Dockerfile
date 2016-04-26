# Dockerfile to create a base container for the IM service
FROM ubuntu:14.04
LABEL description="base container image to run the IM service. (http://www.grycap.upv.es/im)"

# Update and install all the neccesary packages
RUN apt-get update && apt-get install -y \
    gcc \
    python-dev \
    python-pip \
    python-soappy \
    python-pbr \
    python-dateutil \
    python-mock \
    python-nose \
    openssh-client \
    sshpass \
    git \
    libssl-dev \
    libffi-dev \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# Install CherryPy to enable HTTPS in REST API
RUN pip install CherryPy pyOpenSSL
