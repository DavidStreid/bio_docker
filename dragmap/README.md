# Build image and run container
```
docker image build -t dragmap .
# Bring up options
docker run -it --entrypoint /usr/bin/dragen-os --help 
# Run map/align
docker run -it --entrypoint /usr/bin/dragen-os -r /home/data/reference/ -1 reads_1.fastq.gz -2 reads_2.fastq.gz >  result.sam
```

## For more information on options, see [DRAGMAP documentation](https://github.com/Illumina/DRAGMAP)

# Run DRAGMAP
```
java -jar  /usr/local/bioinformatics/picard.jar  # Installed to /usr/bin/
```
