# Preprocessing
* Add "chr" to start of each line

```
mv G1000_loci_hg38_chr1.txt G1000_loci_hg38_chr1.txt_original
sed 's/^/chr/g' G1000_loci_hg38_chr1.txt_original > G1000_loci_hg38_chr1.txt
```
