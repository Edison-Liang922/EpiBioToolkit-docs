# Filter by F-statistic

Keep SNPs with F statistic greater than a threshold.

## Usage

``` r
Bio_MR_filter_f(exposure_dat, f_col = "F_statistic", f_thresh = 10)
```

## Arguments

- exposure_dat:

  data.frame with `F_statistic`.

- f_col:

  Character. Column name for F statistic.

- f_thresh:

  Numeric. Keep rows with `F_statistic > f_thresh`.

## Value

A filtered data.frame.
