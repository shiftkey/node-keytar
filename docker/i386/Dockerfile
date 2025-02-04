FROM i386/debian:bullseye

RUN apt-get update
RUN apt-get install --quiet --yes \
    build-essential \
    curl \
    pkg-config \
    clang \
    python \
    libsecret-1-dev

RUN curl -sL 'https://unofficial-builds.nodejs.org/download/release/v20.12.2/node-v20.12.2-linux-x86.tar.xz' | xzcat | tar -vx  --strip-components=1 -C /usr/local/

RUN node -v

ENV CC clang
ENV CXX clang++
ENV npm_config_clang 1
