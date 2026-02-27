# Run MR methods

Execute Mendelian Randomization methods using TwoSampleMR.

## Usage

``` r
Bio_MR_run_methods(
  harmonized_dat,
  method_list = c("mr_ivw", "mr_egger_regression", "mr_weighted_median",
    "mr_simple_mode", "mr_weighted_mode", "mr_wald_ratio")
)
```

## Arguments

- harmonized_dat:

  data.frame. Harmonised exposure-outcome data.

- method_list:

  Character vector. Methods passed to
  [`TwoSampleMR::mr`](https://mrcieu.github.io/TwoSampleMR/reference/mr.html).

## Value

A data.frame of MR results.
