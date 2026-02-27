# Lasso Feature Selection (Binary Outcome)

Convenience wrapper for Lasso (elastic net with alpha = 1).

## Usage

``` r
Epi_Lasso(
  data,
  outcome_col,
  predictors,
  positive_label = NULL,
  negative_label = NULL,
  nlambda = 100,
  nfolds = 10,
  lambda_choice = c("min", "1se"),
  standardize = TRUE,
  remove_na = TRUE,
  seed = NULL
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

- nlambda:

  Number of lambda values.

- nfolds:

  Number of CV folds.

- lambda_choice:

  Which lambda to use: \`"min"\` or \`"1se"\`.

- standardize:

  Whether to standardize predictors (passed to glmnet).

- remove_na:

  Logical; whether to drop rows with missing values.

- seed:

  Optional random seed for CV.

## Value

Same as \`Epi_ElasticNet\`.
