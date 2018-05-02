FROM ubuntu:latest

ENV DEBIAN_FRONTEND noninteractive

RUN set -e \
      && ln -sf /bin/bash /bin/sh

RUN set -e \
      && apt-get -y update \
      && apt-get -y upgrade \
      && apt-get -y install aptitude curl libffi-dev libssl-dev \
                            python-crypto python-dev python-pip ssh sudo \
      && apt-get -y autoremove \
      && apt-get clean

RUN set -e \
      && pip install -U --no-cache-dir ansible pip pyopenssl

ENTRYPOINT ["/bin/bash", "-c"]
