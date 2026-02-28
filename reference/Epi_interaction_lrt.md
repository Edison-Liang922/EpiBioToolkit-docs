# Interaction LRT for Logistic/Cox Models

Compare models with and without an interaction term using likelihood
ratio test.

## Usage

``` r
Epi_interaction_lrt(
  data,
  model_type = c("logistic", "cox"),
  outcome_col = NULL,
  time_col = NULL,
  status_col = NULL,
  predictors,
  interaction_term,
  positive_label = NULL,
  negative_label = NULL,
  event_label = NULL,
  censor_label = NULL,
  remove_na = TRUE,
  ties = "efron",
  ...
)
```

## Arguments

- data:

  A data frame containing outcome and predictors.

- model_type:

  Character. Either `"logistic"` or `"cox"`.

- outcome_col:

  Column name for binary outcome (logistic only).

- time_col:

  Column name for survival time (cox only).

- status_col:

  Column name for event status (cox only).

- predictors:

  Character vector of main-effect predictors.

- interaction_term:

  Character. Interaction term like `"treatment:biomarker"`.

- positive_label:

  Optional value in \`outcome_col\` mapped to 1 (logistic).

- negative_label:

  Optional value in \`outcome_col\` mapped to 0 (logistic).

- event_label:

  Optional value in \`status_col\` mapped to 1 (cox).

- censor_label:

  Optional value in \`status_col\` mapped to 0 (cox).

- remove_na:

  Logical; whether to drop rows with missing values.

- ties:

  Ties method for
  [`survival::coxph`](https://rdrr.io/pkg/survival/man/coxph.html) (cox
  only).

- ...:

  Additional arguments passed to `glm` or
  [`survival::coxph`](https://rdrr.io/pkg/survival/man/coxph.html).

## Value

A list with \`lrt_table\`, \`p_value\`, and fitted models.
