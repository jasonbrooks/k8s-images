FROM fedora/kubernetes-master
MAINTAINER http://fedoraproject.org/wiki/Cloud

COPY launch.sh /usr/bin/kube-controller-manager-docker.sh

ENTRYPOINT ["/usr/bin/kube-controller-manager-docker.sh"]
