FROM centos:7

# nextflow only needs JRE
RUN yum -y install java-1.8.0-openjdk

ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.292.b10-1.el7_9.x86_64/jre
ENV PATH="${JAVA_HOME}/bin:${PATH}"

RUN cd /usr/local/bin && curl -s https://get.nextflow.io | bash
