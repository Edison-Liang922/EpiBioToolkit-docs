# Run MR analysis for a list of harmonised datasets

Perform MR analysis and write results for each exposure-outcome pair.

## Usage

``` r
Bio_MR_run_batch(
  harmonized_list,
  out_dir,
  cores = 10,
  method_list = c("mr_ivw", "mr_egger_regression", "mr_weighted_median",
    "mr_simple_mode", "mr_weighted_mode", "mr_wald_ratio")
)
```

## Arguments

- harmonized_list:

  List of harmonised data.frames.

- out_dir:

  Character. Output directory.

- cores:

  Integer. Number of cores for parallel processing.

- method_list:

  Character vector. Methods passed to `Bio_MR_run_single`.

## Value

A character vector of completed exposure names.
