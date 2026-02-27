# Format exposure data for TwoSampleMR

Convert a raw GWAS exposure table into TwoSampleMR exposure format using
column mappings.

## Usage

``` r
Bio_MR_format_exposure(
  raw_data,
  phenotype_name,
  col_map = list(snp = "SNP", beta = "BETA", se = "SE", eaf = "EAF", effect_allele =
    "A1", other_allele = "A2", pval = "P", n = "N", chr = "CHR", pos = "POS"),
  pval_filter = NULL,
  pval_col = NULL
)
```

## Arguments

- raw_data:

  data.frame. Raw GWAS exposure data.

- phenotype_name:

  Character. Exposure phenotype name.

- col_map:

  Named list mapping standard names to input columns. Must include: snp,
  beta, se, eaf, effect_allele, other_allele, pval, n, chr, pos.

- pval_filter:

  Optional numeric. If provided, filter raw data before formatting using
  `pval < pval_filter`.

- pval_col:

  Optional character. If provided, overrides `col_map$pval` for the
  pre-filter step.

## Value

A data.frame in TwoSampleMR exposure format.
