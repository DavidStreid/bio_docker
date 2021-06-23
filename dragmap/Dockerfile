FROM centos:7

# Needed to get DRAGMAP
RUN yum -y install git

# Needed to install DRAGMAP
RUN yum -y groupinstall 'Development Tools'

# Add boost dependency
ADD boost_1_76_0.tar.xz /
RUN tar -xf boost_1_76_0.tar.xz 
RUN cp -rf /boost_1_76_0/boost /usr/include

# Add zlib dependency
ADD zlib-1.2.11.tar.gz /
RUN cd zlib-1.2.11 && ./configure && make -j4 && make install

RUN git clone https://github.com/Illumina/DRAGMAP.git

# Install dragmap to /usr/bin
RUN yum -y install boost-devel
RUN cd DRAGMAP && HAS_GTEST=0 make && HAS_GTEST=0 make install

