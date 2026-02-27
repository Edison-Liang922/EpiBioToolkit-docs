# Demo data for MLP diagnostic model

Example input data for `Bio_MLP_train`.

## Usage

``` r
mlp_demo
```

## Format

A list with:

- expr:

  Expression matrix (genes x samples).

- labels:

  Data frame with columns `sample` and `label`.

- genes:

  Optional gene set (first column used).

- positive_label:

  Positive class label (character).

## Source

Simulated example for documentation and testing.
