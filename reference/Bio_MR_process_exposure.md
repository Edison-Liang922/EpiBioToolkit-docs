# Process exposure data (pipeline)

A pipeline for exposure processing: format -\> F statistic -\> clumping.

## Usage

``` r
Bio_MR_process_exposure(
  raw_data,
  phenotype_name,
  col_map = list(snp = "SNP", beta = "BETA", se = "SE", eaf = "EAF", effect_allele =
    "A1", other_allele = "A2", pval = "P", n = "N", chr = "CHR", pos = "POS"),
  filter_pval = 1e-05,
  filter_f = 10,
  clump_params = list(perform = TRUE, kb = 10000, r2 = 0.001, pval = 5e-08, local =
    FALSE, plink_bin = NULL, bfile = NULL)
)
```

## Arguments

- raw_data:

  data.frame. Raw GWAS exposure data.

- phenotype_name:

  Character. Exposure name.

- col_map:

  List. Column mapping for `Bio_MR_format_exposure`.

- filter_pval:

  Numeric. P-value threshold for pre-filter.

- filter_f:

  Numeric. F-statistic threshold.

- clump_params:

  List. Clumping parameters:

  - perform

  - kb

  - r2

  - pval

  - local

  - plink_bin

  - bfile

## Value

A processed exposure data.frame, or NULL if no SNPs remain.
