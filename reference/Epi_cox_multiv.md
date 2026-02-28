# Multivariable Cox Regression

Fit multivariable Cox proportional hazards model and return HR/CI table.

## Usage

``` r
Epi_cox_multiv(
  data,
  time_col,
  status_col,
  predictors,
  event_label = NULL,
  censor_label = NULL,
  remove_na = TRUE,
  conf_level = 0.95,
  ties = "efron",
  pvalue_accuracy = 0.001,
  ...
)
```

## Arguments

- data:

  A data frame containing time, status, and predictors.

- time_col:

  Column name for survival time.

- status_col:

  Column name for event status (1 = event, 0 = censored).

- predictors:

  Character vector of predictor terms.

- event_label:

  Optional value in \`status_col\` mapped to 1.

- censor_label:

  Optional value in \`status_col\` mapped to 0.

- remove_na:

  Logical; whether to drop rows with missing values.

- conf_level:

  Confidence level for HR intervals (default 0.95).

- ties:

  Ties method passed to
  [`survival::coxph`](https://rdrr.io/pkg/survival/man/coxph.html)
  (default "efron").

- pvalue_accuracy:

  Accuracy for p-value formatting (if \`scales\` available).

- ...:

  Additional arguments passed to
  [`survival::coxph`](https://rdrr.io/pkg/survival/man/coxph.html).

## Value

A list with \`results\` (HR/CI/P table), \`model\` (coxph object),
\`concordance\`, and \`n\` (used sample size).
