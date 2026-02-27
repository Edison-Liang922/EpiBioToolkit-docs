# LD clumping using local PLINK

Perform LD clumping with a local PLINK binary via
[`ieugwasr::ld_clump`](https://mrcieu.github.io/ieugwasr/reference/ld_clump.html).

## Usage

``` r
Bio_MR_clump_local(exposure_dat, kb = 10000, r2 = 0.001, plink_bin, bfile)
```

## Arguments

- exposure_dat:

  data.frame. TwoSampleMR exposure data with columns `SNP`,
  `pval.exposure`, `id.exposure`.

- kb:

  Numeric. Clumping window size (kb).

- r2:

  Numeric. LD r2 threshold.

- plink_bin:

  Character. Path to PLINK binary.

- bfile:

  Character. Path prefix of reference panel.

## Value

A clumped data.frame.
