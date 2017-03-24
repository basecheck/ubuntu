FROM ubuntu:xenial
MAINTAINER Christopher Davenport <chris@christopherdavenport.tech>

RUN apt-get update \
    && apt-get install -y \
        apt-utils \
        sudo \
        systemd \
    && rm -rf /var/lib/apt/lists/* \
    && rm -Rf /usr/share/doc \
    && rm -Rf /usr/share/man \
    && touch -m -t 200101010101.01 /var/lib/apt/periodic/update-success-stamp \
    && apt-get clean

VOLUME ["/sys/fs/cgroup"]
CMD ["/lib/systemd/systemd"]
