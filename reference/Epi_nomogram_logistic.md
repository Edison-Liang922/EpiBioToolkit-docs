# Nomogram for logistic regression model

Build a logistic regression model with
[`rms::lrm`](https://rdrr.io/pkg/rms/man/lrm.html) and plot a nomogram.

## Usage

``` r
Epi_nomogram_logistic(
  data,
  formula,
  fun = stats::plogis,
  funlabel = "Risk",
  lp = FALSE,
  lrm_args = list(),
  nomogram_args = list(),
  plot = TRUE,
  plot_args = list()
)
```

## Arguments

- data:

  A data.frame containing the outcome and predictors.

- formula:

  A formula for the logistic model, e.g. `status ~ age + sex`. The
  outcome should be binary (0/1 or factor with 2 levels).

- fun:

  Function to transform linear predictor to risk. Default is
  [`stats::plogis`](https://rdrr.io/r/stats/Logistic.html).

- funlabel:

  Character. Label for the transformed scale.

- lp:

  Logical. Whether to include the linear predictor axis.

- lrm_args:

  List of additional arguments passed to
  [`rms::lrm`](https://rdrr.io/pkg/rms/man/lrm.html).

- nomogram_args:

  List of additional arguments passed to
  [`rms::nomogram`](https://rdrr.io/pkg/rms/man/nomogram.html).

- plot:

  Logical. Whether to draw the nomogram.

- plot_args:

  List of additional arguments passed to
  [`plot()`](https://rdrr.io/r/graphics/plot.default.html).

## Value

A list with:

- `model`: [`rms::lrm`](https://rdrr.io/pkg/rms/man/lrm.html) model.

- `nomogram`:
  [`rms::nomogram`](https://rdrr.io/pkg/rms/man/nomogram.html) object.

- `plot`: recorded base plot if `plot = TRUE`, otherwise NULL.
