# XGBoost multiclass with SHAP (Python)

Train a multiclass XGBoost model via Python xgboost and compute SHAP
values.

## Usage

``` r
Bio_XGB_multiclass(
  X,
  y,
  num_class,
  test_size = 0.2,
  random_state = 0L,
  params = list(eta = 0.1, max_depth = as.integer(6), eval_metric = "mlogloss", nthread =
    as.integer(4), objective = "multi:softprob"),
  num_boost_round = 1000,
  return_shap = TRUE,
  return_confusion = TRUE
)
```

## Arguments

- X:

  Feature matrix/data.frame (samples x features).

- y:

  Integer class labels (0..K-1) or a single-column data.frame.

- num_class:

  Number of classes.

- test_size:

  Test split proportion (default 0.2).

- random_state:

  Random seed for train/test split.

- params:

  XGBoost parameter list. Defaults to a standard multiclass setup.

- num_boost_round:

  Number of boosting rounds.

- return_shap:

  Logical. Whether to compute SHAP values.

- return_confusion:

  Logical. Whether to return a confusion matrix (requires `caret`).

## Value

A list with:

- model:

  Python xgboost booster.

- preds_prob:

  Predicted class probabilities (n x K).

- pred_labels:

  Predicted class labels (0..K-1).

- y_test:

  Test labels (numeric).

- accuracy:

  Classification accuracy.

- confusion:

  Confusion matrix (if requested).

- shap_values:

  SHAP values array (if requested).

- X_test:

  Test feature set (python object).

## Required inputs

- X:

  Rows = samples; columns = features (numeric or factor).

- y:

  Integer labels (0..K-1) with length = nrow(X).
