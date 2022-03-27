FROM tgagor/centos:stream8

RUN echo 'fastestmirror=1' >> /etc/dnf/dnf.conf && \
    dnf install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm && \
    dnf install -y https://rpms.remirepo.net/enterprise/remi-release-8.rpm && \
    dnf module reset -y php && \
    dnf module enable -y php:remi-8.0 && \
    dnf update -y && \
    dnf install -y composer php-pecl-swoole4 && \
    dnf clean all