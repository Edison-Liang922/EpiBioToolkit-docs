# Elastic Net Feature Selection (Binary Outcome)

Fit elastic net logistic regression with cross-validation and select
variables.

## Usage

``` r
Epi_ElasticNet(
  data,
  outcome_col,
  predictors,
  positive_label = NULL,
  negative_label = NULL,
  alpha = 0.5,
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

- alpha:

  Elastic net mixing parameter (0 = ridge, 1 = lasso).

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

A list with:

- cv_fit:

  \`cv.glmnet\` object.

- lambda:

  Selected lambda value.

- coef_table:

  Coefficient table at selected lambda.

- selected_terms:

  Selected predictor terms (non-zero coefficients).
