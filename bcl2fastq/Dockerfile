FROM centos:7

# Install some utilities (needed to install bcl2fastq)
RUN yum -y install rpm cpio

# Install bcl2fastq to /usr/local/bin/ (Ref - https://github.com/litd/docker-cellranger/blob/master/Dockerfile)
RUN cd / && \
  curl http://regmedsrv1.wustl.edu/Public_SPACE/litd/Public_html/pkg/bcl2fastq2-v2.20.0.422-Linux-x86_64.rpm > bcl2fastq2-v2.20.0.422-Linux-x86_64.rpm && \
  rpm2cpio bcl2fastq2-v2.20.0.422-Linux-x86_64.rpm  | cpio -idmv && \
  rm -rf bcl2fastq2-v2.20.0.422-Linux-x86_64.rpm
