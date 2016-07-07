# Overview

Tests are uding docker and travis CI to cover as many as possible distrs.

To run particular distr test locally:

    IMG_NAME=<dist name> IMG_TAG=<version> ANSIBLE_VERSION=<version> ./rundocker

    # example
    IMG_NAME=debian IMG_TAG=jessie ANSIBLE_VERSION=1.9.6 ./rundocker
