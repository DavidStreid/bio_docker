FROM centos:7

# Install JDK for picard (JRE alone won't work)
RUN yum -y install java-1.8.0-openjdk-devel

ENV JAVA_HOME=/usr/lib/jvm/java-openjdk
ENV PATH="${JAVA_HOME}/bin:${PATH}"

RUN mkdir -p /usr/local/bioinformatics

RUN yum -y install git

RUN git clone https://github.com/broadinstitute/picard.git && \
  cd picard && \
  ./gradlew shadowJar && \
  mv build/libs/picard.jar /usr/local/bioinformatics && \
  rm -rf picard
