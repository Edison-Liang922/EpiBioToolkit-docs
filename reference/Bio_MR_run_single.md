# Run MR analysis for one harmonised dataset

Execute MR methods and sensitivity analyses for a single harmonised
dataset.

## Usage

``` r
Bio_MR_run_single(
  harmonized_dat,
  method_list = c("mr_ivw", "mr_egger_regression", "mr_weighted_median",
    "mr_simple_mode", "mr_weighted_mode", "mr_wald_ratio")
)
```

## Arguments

- harmonized_dat:

  data.frame. Harmonised exposure-outcome data.

- method_list:

  Character vector. Methods passed to `Bio_MR_run_methods`.

## Value

A list with elements:

- \`mr_res\`: raw MR results.

- \`or_res\`: OR results.

- \`res_wide\`: wide-format MR results.

- \`heterogeneity\`: heterogeneity results.

- \`pleiotropy\`: pleiotropy results.

- \`steiger\`: Steiger results.

- \`res_all\`: merged final table.
