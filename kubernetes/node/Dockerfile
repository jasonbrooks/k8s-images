FROM fedora
MAINTAINER http://fedoraproject.org/wiki/Cloud

RUN dnf -y update && dnf clean all
RUN dnf -y copr enable jasonbrooks/kubernetes
RUN dnf install -y kubernetes-node && dnf clean all
