# Build image and run container
```
docker image build -t picard .
docker run -it --entrypoint /bin/bash picard
```

# Run picard
```
java -jar  /usr/local/bioinformatics/picard.jar
```
