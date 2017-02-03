FROM fedora:25
MAINTAINER http://fedoraproject.org/wiki/Cloud

RUN dnf -y update && dnf clean all
RUN groupadd -g 994 kube && useradd -u 996 -g 994 kube
RUN dnf install -y kubernetes-master findutils && dnf clean all
