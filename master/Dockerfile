FROM fedora:25
MAINTAINER http://fedoraproject.org/wiki/Cloud

RUN dnf -y update && dnf clean all
RUN dnf install -y kubernetes-master findutils --enablerepo=updates-testing && dnf clean all
