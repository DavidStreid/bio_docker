FROM centos:7

RUN yum -y install rsync

RUN rsync -aP rsync://hgdownload.soe.ucsc.edu/genome/admin/exe/linux.x86_64/liftOver /usr/bin

# See all http://hgdownload.cse.ucsc.edu/goldenpath/${GENOME}}/liftOver/
# RUN curl http://hgdownload.cse.ucsc.edu/goldenpath/hg38/liftOver/hg38ToHg19.over.chain.gz > hg38ToHg19.over.chain.gz
# RUN curl http://hgdownload.cse.ucsc.edu/goldenpath/hg19/liftOver/hg19ToHg38.over.chain.gz > hg19ToHg38.over.chain.gz

RUN gunzip hg38ToHg19.over.chain.gz

ENTRYPOINT ["liftOver"]
