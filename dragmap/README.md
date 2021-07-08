# Build image and run container
```
docker image build -t dragmap .
# Bring up options
docker run dragmap --help
# Run map/align
docker run dragmap -r /home/data/reference/ -1 reads_1.fastq.gz -2 reads_2.fastq.gz >  result.sam
```

## For more information on options, see [DRAGMAP documentation](https://github.com/Illumina/DRAGMAP)

# View Docker Container
```
docker run -it --entrypoint /bin/bash dragmap
```
