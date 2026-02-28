# Decision Curve Analysis (DCA)

Run decision curve analysis using
[`rmda::decision_curve`](https://rdrr.io/pkg/rmda/man/decision_curve.html).

## Usage

``` r
Epi_DCA(
  formula,
  data,
  family = binomial(link = "logit"),
  thresholds = seq(0.01, 0.8, by = 0.01),
  confidence.intervals = 0.95,
  study.design = "cohort",
  plot = TRUE,
  plot_args = list(),
  ...
)
```

## Arguments

- formula:

  Model formula, e.g. `status ~ age + sex`.

- data:

  A data frame used for DCA.

- family:

  Model family (default binomial).

- thresholds:

  Numeric vector of thresholds (default 0.01-0.80).

- confidence.intervals:

  Confidence intervals (default 0.95).

- study.design:

  Study design (default "cohort").

- plot:

  Logical; whether to plot DCA curve.

- plot_args:

  List of additional arguments passed to
  [`rmda::plot_decision_curve`](https://rdrr.io/pkg/rmda/man/plot_decision_curve.html).

- ...:

  Additional arguments passed to
  [`rmda::decision_curve`](https://rdrr.io/pkg/rmda/man/decision_curve.html).

## Value

A list with \`dca\` (decision_curve object) and \`plot\` (ggplot if
plotted).
