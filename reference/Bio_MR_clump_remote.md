# LD clumping using remote API

Perform LD clumping with
[`TwoSampleMR::clump_data`](https://mrcieu.github.io/TwoSampleMR/reference/clump_data.html)
(remote API).

## Usage

``` r
Bio_MR_clump_remote(exposure_dat, kb = 10000, r2 = 0.001)
```

## Arguments

- exposure_dat:

  data.frame. TwoSampleMR exposure data.

- kb:

  Numeric. Clumping window size (kb).

- r2:

  Numeric. LD r2 threshold.

## Value

A clumped data.frame.
