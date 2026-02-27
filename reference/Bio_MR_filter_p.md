# Filter by P-value

Utility function for MR workflows. It filters rows by a P-value
threshold.

## Usage

``` r
Bio_MR_filter_p(data, p_col, p_thresh = 1e-05)
```

## Arguments

- data:

  A data.frame.

- p_col:

  Character. Column name for P-values.

- p_thresh:

  Numeric. Keep rows with `p_col < p_thresh`.

## Value

A filtered data.frame.
