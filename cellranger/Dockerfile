FROM centos:7

# Install some utilities (needed to install bcl2fastq)
RUN yum -y install rpm cpio

# Install cellranger binary to /cellranger-6.0.0/bin/cellranger
RUN cd / && \
  curl http://regmedsrv1.wustl.edu/Public_SPACE/litd/Public_html/pkg/cellranger-6.0.0.tar.gz > cellranger-6.0.0.tar.gz && \
  tar -xzvf cellranger-6.0.0.tar.gz && \
  rm -f cellranger-6.0.0.tar.gz
