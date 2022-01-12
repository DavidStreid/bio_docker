# Build image and run container
```
docker image build -t bcl-convert .
docker run bcl-convert
```

# View Docker Container
```
docker run -it --entrypoint /bin/bash bcl-convert
```
