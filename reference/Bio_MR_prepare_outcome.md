# Prepare outcome data (add phenotype and format)

Wrapper that adds a phenotype column (if missing) and formats outcome
data with `Bio_MR_format_outcome`.

## Usage

``` r
Bio_MR_prepare_outcome(
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

  Named list mapping standard names to input columns.

- phenotype_col:

  Character. Column name used for phenotype.

## Value

A data.frame in TwoSampleMR outcome format.
