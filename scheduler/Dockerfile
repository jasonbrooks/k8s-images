FROM registry.fedoraproject.org/kubernetes-master:f25
MAINTAINER http://fedoraproject.org/wiki/Cloud

ENV NAME=kube-scheduler VERSION=0.1 RELEASE=1 ARCH=x86_64
LABEL BZComponent="$NAME" \
        Name="$FGC/$NAME" \
        Version="$VERSION" \
        Release="$RELEASE.$DISTTAG" \
        Architecture="$ARCH"

COPY launch.sh /usr/bin/kube-scheduler-docker.sh

LABEL RUN /usr/bin/docker run -d --net=host

ENTRYPOINT ["/usr/bin/kube-scheduler-docker.sh"]
