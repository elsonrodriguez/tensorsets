FROM ubuntu:16.04
MAINTAINER Elson Rodriguez <elson.rodriguez@gmail.com>

ENV KUBECTL_VERSION v1.6.4

ADD scripts /scripts
ADD tensorset-controller.sh /

RUN chmod +x /tensorset-controller.sh
RUN chmod +x /scripts/*

ADD https://storage.googleapis.com/kubernetes-release/release/${KUBECTL_VERSION}/bin/linux/amd64/kubectl /usr/local/bin/kubectl
RUN chmod +x /usr/local/bin/kubectl

ADD https://github.com/stedolan/jq/releases/download/jq-1.5/jq-linux64 /usr/local/bin/jq
RUN chmod +x /usr/local/bin/jq

RUN apt-get update && apt-get install -y \
    curl \
    python \
 && rm -rf /var/lib/apt/lists/*

ENTRYPOINT ["/tensorset-controller.sh"]


