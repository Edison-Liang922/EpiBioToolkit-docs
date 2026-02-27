# Pivot MR results to wide format

Convert MR results to a wide table by method.

## Usage

``` r
Bio_MR_pivot_results(mr_res)
```

## Arguments

- mr_res:

  data.frame. MR results with columns `method`, `b`, `se`, `pval`, `or`,
  `or_lci95`, `or_uci95`, `estimate`.

## Value

A wide data.frame (one row per exposure-outcome pair).
