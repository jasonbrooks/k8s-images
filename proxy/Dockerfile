FROM registry.fedoraproject.org/kubernetes-node:25
MAINTAINER http://fedoraproject.org/wiki/Cloud

ENV NAME=kube-proxy VERSION=0.1 RELEASE=1 ARCH=x86_64
LABEL BZComponent="$NAME" \
        Name="$FGC/$NAME" \
        Version="$VERSION" \
        Release="$RELEASE.$DISTTAG" \
        Architecture="$ARCH"

RUN dnf install -y iptables && dnf clean all

LABEL RUN /usr/bin/docker run -d --privileged --net=host 

COPY launch.sh /usr/bin/kube-proxy-docker.sh

ENTRYPOINT ["/usr/bin/kube-proxy-docker.sh"]

