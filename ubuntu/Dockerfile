FROM ubuntu

RUN set -e \
      && ln -sf /bin/bash /bin/sh

RUN set -e \
      && apt-get -y update \
      && apt-get -y upgrade \
      && apt-get -y install curl \
      && apt-get clean

ENTRYPOINT ["/bin/bash", "-c"]
