FROM amd64/centos:centos7

# Download illumina's bcl-convert
# SEE - https://support.illumina.com/sequencing/sequencing_software/bcl-convert/downloads.html

# Versions: 3.6, 3.8, 3.9
ADD bcl-convert-*.rpm /tmp/			
# Version: 3.7
ADD BCLConvertv3.7.5forCentOS7.rpm /tmp/	

RUN yum install -y gdb

# Either works
# RUN rpm -i /tmp/bcl-convert-3.6.3-1.el7.x86_64.rpm			
RUN rpm -i /tmp/BCLConvertv3.7.5forCentOS7.rpm			

# Both Fail
#   what():  Assertion failed in /data/jenkins/workspace/dragen_release_3.8/src/host/dragend/dragend_clientafu.cpp line 68 -- false -- Cache line size 0 doesn't match CACHE_LINE_SIZE=64
# RUN rpm -i /tmp/bcl-convert-3.9.3-2.el7.x86_64.rpm			# FAILED
# RUN rpm -i /tmp/bcl-convert-3.8.2_12_g85770e0b-2.el7.x86_64.rpm	# FAILED

ENTRYPOINT ["/usr/bin/bcl-convert"]
