---
title: Setup
---

## Compute platform

This workshop is designed to be conducted on the [REANNZ](https://www.reannz.co.nz/) compute infrastructure. All software and data are already set up for you to use during the workshop.

## Software used

If you are attempting to work through this material on a non-NeSI compute system, the following software will need to be installed:

| Software  | Version | Manual      | Description 	|
|-----------|---------|-------------|---------------|
| BCFtools  | 1.22    | [link](https://samtools.github.io/bcftools/) | Variant calling | 
| FastQC    | 0.12.1  | [link](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)| Read QA/QC |
| dorado    | v2.1.2  | [link](https://github.com/nanoporetech/dorado) | GPU basecaller for ONT POD5/FAST5 data |
| Nanoplot  | 1.43.0  | [link](https://github.com/wdecoster/NanoPlot) | QA/QC for ONT reads | 
| SAMtools  | 1.25    | [link](http://www.htslib.org/doc/samtools.html) | Read mapping |


## Data availability

The data utilised in this workshop are publicly available:

[https://epi2me.nanoporetech.com/nomiss_96bc_p2i_sup_2026/](https://epi2me.nanoporetech.com/nomiss_96bc_p2i_sup_2026/)

Data relating to the first 3 barcodes along with a random selection of unclassifed reads were extracted from the first three POD5 
files:

```
PBK98658_853a956f_57f83f46_0.pod5
PBK98658_853a956f_57f83f46_1.pod5
PBK98658_853a956f_57f83f46_2.pod5
```

These reads were reconstituted as a set of three POD5 files that were used in this workshop.

`dorado`, `samtools` and ONT's `pod5` software (see below) were used for this. Data from the `.pod5` files above 
were basecalled and split by barcode, read IDs for the first three barcodes were extracted (along with 1% of unclasified reads), 
and the matching reads were then extracted from the original POD5 files via `pod5 filter` to create a small data set for 
use in this workshop.

[https://github.com/nanoporetech/pod5-file-format](https://github.com/nanoporetech/pod5-file-format)

{% include links.md %}
