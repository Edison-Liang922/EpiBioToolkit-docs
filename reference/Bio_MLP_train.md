# Train an MLP diagnostic model (binary classification)

Train a Keras MLP model using gene expression data and binary labels,
and return predictions and evaluation metrics.

## Usage

``` r
Bio_MLP_train(
  expr,
  labels,
  genes = NULL,
  positive_label = "Disease",
  sample_col = "sample",
  label_col = "label",
  split_ratio = 0.8,
  split_index = NULL,
  seed = 123,
  scale_features = TRUE,
  epoch = 100,
  batch_size = 20,
  learning_rate = 0.01,
  hidden_units = c(32, 16, 8),
  dropout = 0.2,
  threshold = 0.5,
  verbose = 1
)
```

## Arguments

- expr:

  A numeric matrix or data.frame of expression values. Rows are genes
  and columns are samples.

- labels:

  A vector of labels (with sample names) or a data.frame containing
  sample IDs and labels.

- genes:

  Optional vector of gene IDs to use as features. If NULL, use all genes
  in `expr`. If a data.frame, the first column is used.

- positive_label:

  Character. Label name for the positive class.

- sample_col:

  Character. Column name in `labels` for sample IDs (when `labels` is a
  data.frame). Default `"sample"`.

- label_col:

  Character. Column name in `labels` for labels (when `labels` is a
  data.frame). Default `"label"`.

- split_ratio:

  Numeric. Training set ratio (0-1). Default 0.8.

- split_index:

  Optional integer vector of training sample indices.

- seed:

  Integer. Random seed for splitting.

- scale_features:

  Logical. Whether to scale features.

- epoch:

  Integer. Training epochs.

- batch_size:

  Integer. Batch size.

- learning_rate:

  Numeric. Learning rate for Adam.

- hidden_units:

  Integer vector. Units per hidden layer.

- dropout:

  Numeric. Dropout rate for hidden layers.

- threshold:

  Numeric. Probability threshold for class prediction.

- verbose:

  Integer. Keras fit verbosity.

## Value

A list with:

- `model`: trained Keras model.

- `history`: training history.

- `evaluation`: test evaluation metrics.

- `prediction`: data.frame with predicted probabilities and labels.

- `confusion`: confusion matrix
  ([`caret::confusionMatrix`](https://rdrr.io/pkg/caret/man/confusionMatrix.html)).

- `roc`: ROC object
  ([`pROC::roc`](https://rdrr.io/pkg/pROC/man/roc.html)).
