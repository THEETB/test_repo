ARG RELEASE_TAG
FROM centos:${RELEASE_TAG}
#FROM rhel:8.2-299

RUN sed -i -e "s|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g" /etc/yum.repos.d/CentOS-* \
    #&& sed -i -e "s|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g" /etc/yum.repos.d/CentOS-* \
    && sed -i 's/vault.centos.org/mirror.rackspace.com\/centos-vault/g' /etc/yum.repos.d/CentOS-Linux-*.repo


RUN dnf update -y \
    && dnf -y install dnf-plugins-core \
    && dnf -y install https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm \
    && dnf install langpacks-en glibc-all-langpacks -y \
    && dnf config-manager --set-enabled powertools \
    && dnf grouplist \
    && dnf install -y gcc-c++-8.5.0-4.el8_5.x86_64
    #&& dnf -y install java-1.8.0-openjdk-devel
