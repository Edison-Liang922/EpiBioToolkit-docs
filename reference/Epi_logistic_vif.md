# VIF Collinearity Diagnosis

Compute VIF for a set of predictors and provide collinearity flags.

## Usage

``` r
Epi_logistic_vif(
  data,
  outcome_col,
  predictors,
  remove_na = TRUE,
  vif_cut_severe = 10,
  vif_cut_moderate = 5
)
```

## Arguments

- data:

  A data frame containing outcome and predictors.

- outcome_col:

  Column name for outcome (binary or numeric).

- predictors:

  Character vector of predictor column names.

- remove_na:

  Logical; whether to drop rows with missing values.

- vif_cut_severe:

  Threshold for severe collinearity (default 10).

- vif_cut_moderate:

  Threshold for moderate collinearity (default 5).

## Value

A list with:

- vif_table:

  Data frame with VIF values and collinearity diagnosis.

- vif_values:

  Named numeric vector of VIF.

- flag:

  Summary flags (severe/moderate).
