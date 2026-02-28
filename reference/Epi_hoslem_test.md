# Hosmer-Lemeshow Goodness-of-Fit Test

Perform Hosmer-Lemeshow test for logistic regression models.

## Usage

``` r
Epi_hoslem_test(
  observed,
  predicted,
  g = 10,
  positive_label = NULL,
  negative_label = NULL,
  na.rm = TRUE
)
```

## Arguments

- observed:

  Vector of observed outcomes (0/1 or two-level factor).

- predicted:

  Vector of predicted probabilities (0-1).

- g:

  Number of groups (default 10).

- positive_label:

  Optional value in \`observed\` mapped to 1.

- negative_label:

  Optional value in \`observed\` mapped to 0.

- na.rm:

  Logical; remove NA pairs.

## Value

A list with \`table\` (statistic/df/p) and the raw test object.
