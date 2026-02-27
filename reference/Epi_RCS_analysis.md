# Restricted Cubic Spline (RCS) Analysis

Fit RCS logistic models across k values, pick best by AIC, and return
plot data.

## Usage

``` r
Epi_RCS_analysis(
  data,
  outcome_col,
  exposure_col,
  k_values = 3:7,
  positive_label = NULL,
  negative_label = NULL,
  ref_quantile = 0.5,
  conf_int = 0.95,
  remove_na = TRUE
)
```

## Arguments

- data:

  A data frame containing outcome and exposure.

- outcome_col:

  Column name for binary outcome.

- exposure_col:

  Column name for continuous exposure.

- k_values:

  Integer vector of knots to test (default 3:7).

- positive_label:

  Optional value in \`outcome_col\` mapped to 1.

- negative_label:

  Optional value in \`outcome_col\` mapped to 0.

- ref_quantile:

  Quantile for reference value (default 0.5).

- conf_int:

  Confidence level (default 0.95).

- remove_na:

  Logical; whether to drop rows with missing values.

## Value

A list with \`best_k\`, \`aic_table\`, \`model\`, \`anova\`, and
\`plot_data\`.
