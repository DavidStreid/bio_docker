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
DATA_DIR=$(pwd)   # directory w/ data to run through ascat
docker run -it --mount type=bind,source=${DATA_DIR},target=/work_dir,readonly --entrypoint /bin/bash ascat
Rscript work_dir/run_matched_normal.r
```

### DEBUG contianer
```
docker run -it --entrypoint /bin/bash ascat
```

## Required Data
* Ascat uses loci/alleles specific to each chromosome. A pre-generated set derived from the 1000 Genomes project can be downloaded. Below are links to filtering methods for deriving the alleles and download links documented in sarek's nf-core pipeline.
  * [Documentation](https://github.com/VanLoo-lab/ascat/tree/master/ReferenceFiles/WGS)
  * [Download](https://nf-co.re/sarek/usage#where-do-the-used-reference-genomes-originate-from)
    * [hg38 alleles](https://www.dropbox.com/s/uouszfktzgoqfy7/G1000_alleles_hg38.zip)
    * [hg38 loci](https://www.dropbox.com/s/80cq0qgao8l1inj/G1000_loci_hg38.zip)