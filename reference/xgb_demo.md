# Demo data for XGBoost + SHAP

Example input for `Bio_XGB_regression` and `Bio_XGB_multiclass`.

## Usage

``` r
xgb_demo
```

## Format

A list with:

- X:

  Feature data.frame (samples x features).

- y_reg:

  Numeric regression outcome.

- y_cls:

  Integer class labels (0..2).

- class_map:

  Named vector mapping class IDs to labels.

## Source

Simulated example for documentation and testing.
