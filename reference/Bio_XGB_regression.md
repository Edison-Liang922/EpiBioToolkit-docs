# XGBoost regression with SHAP (Python)

Train a regression XGBoost model via Python xgboost and compute SHAP
values.

## Usage

``` r
Bio_XGB_regression(
  X,
  y,
  test_size = 0.2,
  random_state = 0L,
  params = list(eta = 0.1, max_depth = as.integer(6), eval_metric = "rmse", nthread =
    as.integer(4), objective = "reg:squarederror"),
  num_boost_round = 1000,
  return_shap = TRUE
)
```

## Arguments

- X:

  Feature matrix/data.frame (samples x features).

- y:

  Numeric vector or a single-column data.frame for the outcome.

- test_size:

  Test split proportion (default 0.2).

- random_state:

  Random seed for train/test split.

- params:

  XGBoost parameter list. Defaults to a standard regression setup.

- num_boost_round:

  Number of boosting rounds.

- return_shap:

  Logical. Whether to compute SHAP values.

## Value

A list with:

- model:

  Python xgboost booster.

- preds:

  Predictions for the test set.

- y_test:

  Test labels (numeric).

- metrics:

  List with RMSE and R2.

- shap_values:

  SHAP values for the test set (if requested).

- X_test:

  Test feature set (python object).

## Required inputs

- X:

  Rows = samples; columns = features (numeric or factor).

- y:

  Numeric outcome vector (length = nrow(X)).
