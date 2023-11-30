FROM ubuntu:22.04

# Install basic CLI tools etc.
RUN apt-get update && apt-get install -y --fix-missing --no-install-recommends \
        build-essential \
        curl \
        git-core \
        iputils-ping \
        pkg-config \
        rsync \
        software-properties-common \
        unzip \
        wget \
        libcairo2-dev \
        libpango1.0-dev \
        libjpeg-dev \
        libgif-dev \
        librsvg2-dev


# Install NodeJS
RUN curl --silent --location https://deb.nodesource.com/setup_20.x | bash -
RUN apt-get install --yes nodejs

# Clean up commands
RUN apt-get autoremove -y && apt-get clean && \
    rm -rf /usr/local/src/*

RUN apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR "/Users/bogdankozlov/Documents/Projects/Pet/face-api.js/examples/examples-nodejs"
CMD ["/bin/bash"]