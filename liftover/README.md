# Build image and run container
```
docker image build -t liftover .
docker run -it --entrypoint /bin/bash liftover

# e.g.
docekr run -v /path/to/oldFile:/files --entrypoint /bin/bash liftover
```

# Run liftOver
```
docker run liftover

# e.g.
docker run liftover oldFile map.chain newFile unMapped
```
