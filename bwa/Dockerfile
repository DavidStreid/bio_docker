FROM centos:7

RUN curl http://springdale.princeton.edu/data/springdale/7/x86_64/os/RPM-GPG-KEY-springdale > /etc/pki/rpm-gpg/RPM-GPG-KEY-springdale

RUN echo "[computational-core]" > /etc/yum.repos.d/springdale.computational.repo && \
  echo "name=Springdale computational Base \$releasever - \$basearch" >> /etc/yum.repos.d/springdale.computational.repo && \
  echo "#baseurl=file:///springdale/computational/\$releasever/\$basearch" >> /etc/yum.repos.d/springdale.computational.repo && \
  echo "#mirrorlist=http://mirror.math.princeton.edu/pub/springdale/puias/computational/\$releasever/\$basearch/mirrorlist" >> /etc/yum.repos.d/springdale.computational.repo && \
  echo "baseurl=http://springdale.princeton.edu/data/springdale/computational/\$releasever/\$basearch" >> /etc/yum.repos.d/springdale.computational.repo && \
  echo "gpgcheck=1" >> /etc/yum.repos.d/springdale.computational.repo && \
  echo "gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-springdale" >> /etc/yum.repos.d/springdale.computational.repo 

# Installs to /usr/bin/bwa
RUN yum -y install bwa
