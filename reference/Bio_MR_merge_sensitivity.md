# Merge sensitivity results into MR summary table

Combine MR wide results with heterogeneity, pleiotropy, and Steiger
results.

## Usage

``` r
Bio_MR_merge_sensitivity(
  res_wide,
  hetero_res = data.frame(),
  pleio_res = data.frame(),
  steiger_res = data.frame()
)
```

## Arguments

- res_wide:

  data.frame. Output from `Bio_MR_pivot_results`.

- hetero_res:

  data.frame. Output from `Bio_MR_heterogeneity`.

- pleio_res:

  data.frame. Output from `Bio_MR_pleiotropy`.

- steiger_res:

  data.frame. Output from `Bio_MR_steiger`.

## Value

A merged data.frame.
