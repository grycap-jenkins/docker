# Dockerfile to create a base container for the IM service
FROM ubuntu:14.04
LABEL description="Base container image to run python tests."

# Update and install all the neccesary packages
RUN apt-get update && apt-get install -y \
    git \
    curl \
    python-ply \
    python-mock \
    python-nose \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# Install cpyutils
RUN git clone https://github.com/grycap/cpyutils.git /tmp/cpyutils \
 && cd /tmp/cpyutils \
 && python setup.py install

# Install clues
RUN git clone https://github.com/grycap/clues.git /tmp/clues \
 && cd /tmp/clues \
 && python setup.py install
 
# Add jenkins user/group  
RUN groupadd -g 112 devel \
 && useradd -u 105 -g 112 jenkins
