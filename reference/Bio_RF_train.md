# Train a random forest classifier

Train a randomForest model using a feature-by-sample matrix and group
labels.

## Usage

``` r
Bio_RF_train(
  expr,
  group_df,
  sample_col = "Sample",
  group_col = "group",
  group_keep = NULL,
  filter_prop = 0.2,
  scale_data = TRUE,
  scale_by = c("sample", "feature"),
  train_prop = 0.75,
  seed = 1234,
  ntree = 500,
  mtry = NULL,
  importance = TRUE,
  proximity = FALSE,
  positive_class = NULL
)
```

## Arguments

- expr:

  Matrix/data.frame with features in rows and samples in columns.

- group_df:

  data.frame with sample IDs and group labels.

- sample_col:

  Character. Sample ID column name in `group_df`.

- group_col:

  Character. Group label column name in `group_df`.

- group_keep:

  Optional vector of group labels to keep. If NULL, use all.

- filter_prop:

  Numeric (0-1). Keep features with \> `filter_prop` of samples having
  values \> 0. Set NULL to skip filtering.

- scale_data:

  Logical. Whether to scale data before modeling.

- scale_by:

  Character. `"sample"` scales by sample (columns), `"feature"` scales
  by feature (rows). Only used when `scale_data = TRUE`.

- train_prop:

  Numeric (0-1). Training set proportion.

- seed:

  Integer. Random seed for splitting.

- ntree:

  Integer. Number of trees.

- mtry:

  Integer. Number of variables randomly sampled at each split.

- importance:

  Logical. Whether to compute variable importance.

- proximity:

  Logical. Whether to compute proximity.

- positive_class:

  Character. Positive class label for ROC. If NULL and binary, uses the
  second factor level.

## Value

A list with:

- `model`: trained randomForest model.

- `train`: list with `prob`, `pred`, `confusion`, and `accuracy`.

- `test`: list with `prob`, `pred`, `confusion`, and `accuracy`.

- `importance`: data.frame of variable importance (type 1).

- `roc_train`: ROC object (binary only) or NULL.

- `roc_test`: ROC object (binary only) or NULL.
