# Build image and run container
```
docker image build -t cellranger .
docker run -it --entrypoint /bin/bash cellranger
```
# Run cellranger
```
cellranger 		# Should be installed at /opt/cellranger/cellranger-6.0.0/bin/cellranger
```
