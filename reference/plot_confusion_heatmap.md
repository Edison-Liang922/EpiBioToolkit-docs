# Confusion matrix heatmap

Plot a confusion matrix as a heatmap with counts.

## Usage

``` r
plot_confusion_heatmap(
  cm,
  label_map = NULL,
  low = "white",
  high = "blue",
  save_path = NULL,
  width = 8,
  height = 6
)
```

## Arguments

- cm:

  A
  [`caret::confusionMatrix`](https://rdrr.io/pkg/caret/man/confusionMatrix.html)
  object, a matrix, or a table.

- label_map:

  Optional named vector for relabeling classes (e.g.,
  `c("0"="Normal","1"="Osteopenia","2"="Osteoporosis")`).

- low:

  Low color for gradient.

- high:

  High color for gradient.

- save_path:

  Optional. File path to save the plot.

- width:

  Width for saved plot.

- height:

  Height for saved plot.

## Value

A ggplot object.

## Required inputs

- cm:

  Confusion matrix object or matrix/table.
