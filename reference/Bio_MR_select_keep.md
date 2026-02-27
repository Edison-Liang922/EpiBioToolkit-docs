# Filter by mr_keep column

Utility function for MR workflows. It keeps rows where `mr_keep` (or a
specified column) is TRUE.

## Usage

``` r
Bio_MR_select_keep(data, keep_col = "mr_keep", keep_value = TRUE)
```

## Arguments

- data:

  A data.frame.

- keep_col:

  Character. Column name used for keep flag.

- keep_value:

  Logical. Value to keep (default TRUE).

## Value

A filtered data.frame.
