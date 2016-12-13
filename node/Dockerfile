FROM registry.fedoraproject.org/fedora:25
MAINTAINER http://fedoraproject.org/wiki/Cloud

ENV NAME=kubernetes-node VERSION=0.1 RELEASE=1 ARCH=x86_64
LABEL BZComponent="$NAME" \
        Name="$FGC/$NAME" \
        Version="$VERSION" \
        Release="$RELEASE.$DISTTAG" \
        Architecture="$ARCH"

RUN dnf -y update && dnf clean all
RUN dnf install -y kubernetes-node findutils && dnf clean all
