# Ascat 
**Description**: Tool used to estimate tumour purity, tumor Ploidy, & allele-specific copy number profiles
* [Example Usage](https://github.com/VanLoo-lab/ascat/blob/e42dc4fcbb3d279546c976d263c981b0d83b4ff3/ExampleData/README.md)
* Dependencies - [alleleCount](https://github.com/cancerit/alleleCount) for allele counting
* [Documentation](https://github.com/VanLoo-lab/ascat/blob/master/man/ASCAT-manual.pdf)
  * [Common Usages Runbook](https://github.com/VanLoo-lab/ascat/blob/e42dc4fcbb3d279546c976d263c981b0d83b4ff3/ExampleData/README.md)

## Build image and run container
```
docker image build -t ascat .
```

## View Docker Container
```
DATA_DIR=... # directory w/ data to run through ascat
docker run -it --mount type=bind,source=${DATA_DIR},target=/data,readonly --entrypoint /bin/bash ascat
```

### DEBUG contianer
```
docker run -it --entrypoint /bin/bash ascat
```
