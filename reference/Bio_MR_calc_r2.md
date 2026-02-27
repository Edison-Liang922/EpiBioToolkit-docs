# Calculate R2 for exposure instruments

Compute per-SNP R2 using beta, se, sample size, and EAF.

## Usage

``` r
Bio_MR_calc_r2(
  exposure_dat,
  beta_col = "beta.exposure",
  se_col = "se.exposure",
  n_col = "samplesize.exposure",
  eaf_col = "eaf.exposure"
)
```

## Arguments

- exposure_dat:

  data.frame. TwoSampleMR exposure data.

- beta_col:

  Character. Column name for beta.

- se_col:

  Character. Column name for standard error.

- n_col:

  Character. Column name for sample size.

- eaf_col:

  Character. Column name for effect allele frequency.

## Value

A data.frame with an added `R2` column.
