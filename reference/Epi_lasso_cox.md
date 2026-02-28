# Lasso Cox Regression

Fit Lasso Cox model with cross-validation using
[`glmnet::cv.glmnet`](https://rdrr.io/pkg/glmnet/man/cv.glmnet.html).

## Usage

``` r
Epi_lasso_cox(
  data,
  time_col,
  status_col,
  predictors,
  event_label = NULL,
  censor_label = NULL,
  remove_na = TRUE,
  nfolds = 10,
  lambda_choice = c("min", "1se"),
  standardize = TRUE,
  seed = NULL,
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

- nfolds:

  Number of CV folds (default 10).

- lambda_choice:

  Which lambda to use: `"min"` or `"1se"`.

- standardize:

  Whether to standardize predictors (default TRUE).

- seed:

  Optional random seed for CV.

- ...:

  Additional arguments passed to
  [`glmnet::cv.glmnet`](https://rdrr.io/pkg/glmnet/man/cv.glmnet.html).

## Value

A list with \`cv_fit\`, \`lambda\`, \`coef_table\`, \`selected_terms\`,
\`cindex\` (if compute possible), and \`x\`/\`y\` used in fitting.
