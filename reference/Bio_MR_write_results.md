# Write MR results to files

Save MR results and assumptions into Excel/CSV files.

## Usage

``` r
Bio_MR_write_results(
  res_all,
  results_or,
  assumption,
  out_prefix,
  overwrite = TRUE
)
```

## Arguments

- res_all:

  data.frame. Final merged MR results table.

- results_or:

  data.frame. OR results from `Bio_MR_calc_or`.

- assumption:

  data.frame. Assumption table (SNP, p-values, mr_keep).

- out_prefix:

  Character. Prefix for output files (without extension).

- overwrite:

  Logical. Whether to overwrite existing files.

## Value

A list of output file paths.
