# Harmonise a list of exposures with one outcome

Perform harmonisation for a list of exposure datasets in parallel.

## Usage

``` r
Bio_MR_harmonize_list(exposure_list, outcome_dat, cores = 10)
```

## Arguments

- exposure_list:

  List of TwoSampleMR exposure data.frames.

- outcome_dat:

  TwoSampleMR outcome data.frame.

- cores:

  Integer. Number of cores for parallel processing.

## Value

A list of harmonised data.frames (filtered for non-empty results).
