FROM centos:centos7
MAINTAINER The CentOS Project <cloud-ops@centos.org>

RUN yum -y update && yum clean all
RUN cd /etc/yum.repos.d && curl https://copr.fedorainfracloud.org/coprs/jasonbrooks/kubernetes/repo/epel-7/jasonbrooks-kubernetes-epel-7.repo
RUN yum install -y kubernetes-master && yum clean all
