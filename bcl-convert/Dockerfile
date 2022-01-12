FROM amd64/centos:centos7

# Download illumina's bcl-convert
# SEE - https://support.illumina.com/sequencing/sequencing_software/bcl-convert/downloads.html

# Add downloaded RPM package to image 
ADD bcl-convert-*.rpm /tmp/

RUN yum install -y gdb

# RUN rpm -i /tmp/bcl-convert-3.9.3-2.el7.x86_64.rpm			# FAILED
# RUN rpm -i /tmp/bcl-convert-3.8.2_12_g85770e0b-2.el7.x86_64.rpm	# FAILED
RUN rpm -i /tmp/bcl-convert-3.6.3-1.el7.x86_64.rpm

ENTRYPOINT ["/usr/bin/bcl-convert"]
