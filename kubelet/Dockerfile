FROM registry.fedoraproject.org/kubernetes-node:25
MAINTAINER http://fedoraproject.org/wiki/Cloud

ENV NAME=kubelet VERSION=0.1 RELEASE=1 ARCH=x86_64
LABEL BZComponent="$NAME" \
        Name="$FGC/$NAME" \
        Version="$VERSION" \
        Release="$RELEASE.$DISTTAG" \
        Architecture="$ARCH"

# Containerized kubelet requires nsenter
RUN dnf install -y util-linux && dnf clean all

LABEL RUN=/usr/bin/docker run -d --privileged --net=host --pid=host -v /:/rootfs:ro -v /sys:/sys:rw -v /var/run:/var/run:rw -v /run:/run:rw -v /var/lib/docker:/var/lib/docker:rw -v /var/lib/kubelet:/var/lib/kubelet:slave -v /var/log/containers:/var/log/containers:rw

COPY launch.sh /usr/bin/kubelet-docker.sh

ENTRYPOINT ["/usr/bin/kubelet-docker.sh"]
