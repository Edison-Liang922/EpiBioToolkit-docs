# Stepwise Regression for Binary Outcomes

Perform forward, backward, or both-direction stepwise logistic
regression.

## Usage

``` r
Epi_Stepwise_Regression(
  data,
  outcome_col,
  predictors,
  positive_label = NULL,
  negative_label = NULL,
  direction = c("forward", "backward", "both"),
  trace = 0,
  remove_na = TRUE
)

`Epi_Stepwise-Regression`(
  data,
  outcome_col,
  predictors,
  positive_label = NULL,
  negative_label = NULL,
  direction = c("forward", "backward", "both"),
  trace = 0,
  remove_na = TRUE
)
```

## Arguments

- data:

  A data frame containing outcome and predictors.

- outcome_col:

  Column name for binary outcome.

- predictors:

  Character vector of predictor column names.

- positive_label:

  Optional value in \`outcome_col\` mapped to 1.

- negative_label:

  Optional value in \`outcome_col\` mapped to 0.

- direction:

  Stepwise direction: \`"forward"\`, \`"backward"\`, or \`"both"\`.

- trace:

  Passed to \`stats::step\` (0 = silent).

- remove_na:

  Logical; whether to drop rows with missing values.

## Value

A list with fitted models and selected terms.
