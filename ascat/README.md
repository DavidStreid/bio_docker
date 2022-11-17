# Ascat 
**Description**: Tool used to estimate tumour purity, tumor Ploidy, & allele-specific copy number profiles
* [Example Usage](https://github.com/VanLoo-lab/ascat/blob/e42dc4fcbb3d279546c976d263c981b0d83b4ff3/ExampleData/README.md)
* Dependencies - [alleleCount](https://github.com/cancerit/alleleCount) for allele counting

## Build image and run container
```
docker image build -t ascat .
```

## View Docker Container
```
docker run -it --entrypoint /bin/bash ascat
```
