FROM jasonbrooks/fedora:25
MAINTAINER http://fedoraproject.org/wiki/Cloud

RUN dnf -y update && dnf clean all
RUN cd /etc/yum.repos.d && curl https://copr.fedorainfracloud.org/coprs/jasonbrooks/kubernetes/repo/fedora-25/jasonbrooks-kubernetes-fedora-25.repo
RUN dnf install -y kubernetes-master findutils && dnf clean all
