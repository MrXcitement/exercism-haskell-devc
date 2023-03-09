## Build a haskel GHCup based image and exercism cli
## Note: on local arm64/Apple Silicon do not use -buster variants 
## https://github.com/devcontainers/images/tree/main/src/gojk
FROM mcr.microsoft.com/devcontainers/go

# Update system and install GHCup requirements
RUN apt-get update \
    && apt-get -y upgrade \
    && DEBIAN_FRONTEND=noninteractive apt-get -y install --no-install-recommends \
        build-essential \
        curl \
        libffi-dev \
        libgmp-dev \
        libgmp10 \
        libncurses-dev \
        libncurses5 \
        libnuma-dev \
        libtinfo5 \
        llvm \
    && apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*

# Install the exercism client
RUN go install -x github.com/exercism/cli/exercism@latest

# Switch to the vscode user
USER vscode

# Install GCHup into their home directory
RUN curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | sh \
    && echo PATH="$HOME/.cabal/bin:$HOME/.ghcup/bin:$PATH" >> "$HOME/.profile"
