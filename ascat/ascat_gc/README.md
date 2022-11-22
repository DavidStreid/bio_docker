# ascat GC correction file
* [Documentation](https://github.com/VanLoo-lab/ascat/tree/master/ReferenceFiles/WGS)
* [Download](https://nf-co.re/sarek/usage#where-do-the-used-reference-genomes-originate-from)
  * [hg38 gc](https://www.dropbox.com/s/n7g5dh0ld1hcto8/GC_G1000_hg38.zip) 

## Pre-processing
* Add `chr` to scaffold column (col 2)

```
gc_correction_file <- "/work_dir/ascat_gc/GC_G1000_hg38.txt"
```