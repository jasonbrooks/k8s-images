FROM fedora:25
MAINTAINER http://fedoraproject.org/wiki/Cloud

RUN dnf -y update && dnf clean all
RUN dnf install -y kubernetes-node findutils && dnf clean all
