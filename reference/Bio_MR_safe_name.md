# Sanitize names for file output

Utility function for MR workflows. It replaces characters that are
unsafe for file names.

## Usage

``` r
Bio_MR_safe_name(x, replace_with = "_")
```

## Arguments

- x:

  Character vector of names.

- replace_with:

  Character. Replacement string for unsafe characters.

## Value

A character vector with sanitized names.
