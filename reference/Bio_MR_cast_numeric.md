# Coerce columns to numeric

Utility function for MR workflows. It converts specified columns to
numeric. Non-convertible values become NA with a warning from
`as.numeric`.

## Usage

``` r
Bio_MR_cast_numeric(data, cols)
```

## Arguments

- data:

  A data.frame.

- cols:

  Character vector of column names to convert.

## Value

A data.frame with selected columns converted to numeric.
