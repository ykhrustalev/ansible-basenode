FROM ubuntu:12.04

RUN apt-get update \
    && apt-get install -y --no-install-recommends --no-install-suggests \
        build-essential \
        python-setuptools \
        python-dev \
        libssl-dev \
        libffi-dev \
    && easy_install pip \
    && pip install -U setuptools \
    && pip install -U wheel \
    && pip install \
        `# common ansible` \
        pycrypto \
        cryptography \
        jinja2 \
        paramiko \
        PyYAML \
    && rm -rf /var/lib/apt/lists/* /root/.cache
