# Check required columns in a data.frame

Utility function for MR workflows. It checks whether required columns
exist in the input data.

## Usage

``` r
Bio_MR_check_cols(data, required_cols, data_name = "data", strict = TRUE)
```

## Arguments

- data:

  A data.frame to check.

- required_cols:

  Character vector of required column names.

- data_name:

  Character. Name used in error messages.

- strict:

  Logical. If TRUE (default), stop when columns are missing. If FALSE,
  return the missing column names.

## Value

If `strict = TRUE`, returns `TRUE` invisibly when all required columns
are present. If `strict = FALSE`, returns a character vector of missing
columns (length 0 if none missing).
