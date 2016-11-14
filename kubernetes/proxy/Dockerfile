FROM fedora/kubernetes-node
MAINTAINER http://fedoraproject.org/wiki/Cloud

RUN dnf install -y iptables && dnf clean all

LABEL RUN='/usr/bin/docker run -d --net=host --privileged ${OPT1} --name ${NAME} ${IMAGE} ${OPT3}'

COPY launch.sh /usr/bin/kube-proxy-docker.sh

ENTRYPOINT ["/usr/bin/kube-proxy-docker.sh"]

