# Calculate F-statistic from R2

Compute per-SNP F statistics using R2 and sample size.

## Usage

``` r
Bio_MR_calc_f(exposure_dat, r2_col = "R2", n_col = "samplesize.exposure")
```

## Arguments

- exposure_dat:

  data.frame. TwoSampleMR exposure data with `R2`.

- r2_col:

  Character. Column name for R2.

- n_col:

  Character. Column name for sample size.

## Value

A data.frame with an added `F_statistic` column.
