# LD clumping dispatcher

Select local or remote clumping based on parameters.

## Usage

``` r
Bio_MR_clump_dispatch(
  exposure_dat,
  perform = TRUE,
  kb = 10000,
  r2 = 0.001,
  pval_thresh = NULL,
  local = FALSE,
  plink_bin = NULL,
  bfile = NULL
)
```

## Arguments

- exposure_dat:

  data.frame. TwoSampleMR exposure data.

- perform:

  Logical. If FALSE, returns input unchanged.

- kb:

  Numeric. Clumping window size (kb).

- r2:

  Numeric. LD r2 threshold.

- pval_thresh:

  Numeric. Optional p-value filter before clumping.

- local:

  Logical. If TRUE, use local PLINK clumping.

- plink_bin:

  Character. Path to PLINK binary (local only).

- bfile:

  Character. Path prefix of reference panel (local only).

## Value

A clumped data.frame (or original if `perform = FALSE`).
