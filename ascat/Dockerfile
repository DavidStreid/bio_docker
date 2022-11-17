FROM centos:7

# Install EPEL repositories (with R)
RUN yum -y install epel-release

# Install R
RUN yum -y install R

# Install Packages (Select Mirror - # 76: USA (MO) [https])
# BiocManager
RUN R -e "chooseCRANmirror(ind = 76); install.packages('BiocManager'); install.packages('devtools')"

# Devtools
# Requires following yum packages
RUN yum -y install libcurl-devel openssl-devel libgit2-devel libxml2-devel harfbuzz-devel fribidi-devel freetype-devel libpng-devel libtiff-devel libjpeg-turbo-devel
RUN R -e "chooseCRANmirror(ind = 76); install.packages('devtools')"

RUN R -e "BiocManager::install(c('GenomicRanges','IRanges'), force = TRUE)"
RUN R -e "devtools::install_github('VanLoo-lab/ascat/ASCAT', force = TRUE)"

# Install alleleCount (dependency for ASCAT)
RUN yum -y install git
RUN git clone https://github.com/cancerit/alleleCount.git

# Install package dependencies for alleleCount & alleleCount
RUN yum -y install bzip2 wget perl-core
RUN yum -y groupinstall 'Development Tools'
RUN cd /alleleCount && ./setup.sh /usr/local
