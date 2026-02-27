# Format outcome data for TwoSampleMR

Convert a raw GWAS outcome table into TwoSampleMR outcome format using
column mappings.

## Usage

``` r
Bio_MR_format_outcome(
  raw_data,
  phenotype_name = "Outcome",
  col_map = list(snp = "SNP", beta = "BETA", se = "SE", eaf = "EAF", effect_allele =
    "A1", other_allele = "A2", pval = "P", n = "N", chr = "CHR", pos = "POS"),
  phenotype_col = "trait"
)
```

## Arguments

- raw_data:

  data.frame. Raw GWAS outcome data.

- phenotype_name:

  Character. Outcome phenotype name.

- col_map:

  Named list mapping standard names to input columns. Must include: snp,
  beta, se, eaf, effect_allele, other_allele, pval, n, chr, pos.

- phenotype_col:

  Character. Column name in `raw_data` used as phenotype for
  `format_data`. If missing, a new column is created.

## Value

A data.frame in TwoSampleMR outcome format.
