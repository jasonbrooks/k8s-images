FROM registry.fedoraproject.org/kubernetes-master:25
MAINTAINER http://fedoraproject.org/wiki/Cloud

ENV NAME=kube-apiserver VERSION=0.1 RELEASE=1 ARCH=x86_64
LABEL BZComponent="$NAME" \
        Name="$FGC/$NAME" \
        Version="$VERSION" \
        Release="$RELEASE.$DISTTAG" \
        Architecture="$ARCH"

COPY launch.sh /usr/bin/kube-apiserver-docker.sh

LABEL RUN /usr/bin/docker/ run -d --net=host -p 443:443

ENTRYPOINT ["/usr/bin/kube-apiserver-docker.sh"]
