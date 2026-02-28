# KM Survival Curve and Log-rank Test

Fit Kaplan-Meier curves and perform log-rank test.

## Usage

``` r
Epi_km_logrank(
  data,
  time_col,
  status_col,
  group_col,
  event_label = NULL,
  censor_label = NULL,
  remove_na = TRUE,
  times = NULL,
  pvalue_accuracy = 0.001
)
```

## Arguments

- data:

  A data frame containing time, status, and group.

- time_col:

  Column name for survival time.

- status_col:

  Column name for event status (1 = event, 0 = censored).

- group_col:

  Column name for grouping variable.

- event_label:

  Optional value in \`status_col\` mapped to 1.

- censor_label:

  Optional value in \`status_col\` mapped to 0.

- remove_na:

  Logical; whether to drop rows with missing values.

- times:

  Optional numeric vector of time points to summarize survival.

- pvalue_accuracy:

  Accuracy for p-value formatting (if \`scales\` available).

## Value

A list with \`fit\` (survfit), \`logrank\` (survdiff), \`p_value\`,
\`p_value_fmt\`, and optional \`summary_table\` if \`times\` provided.
