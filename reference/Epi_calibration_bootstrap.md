# Bootstrap Calibration Curve (Logistic)

Build bootstrap calibration curve using
[`rms::calibrate`](https://rdrr.io/pkg/rms/man/calibrate.html) on a
logistic model.

## Usage

``` r
Epi_calibration_bootstrap(
  data,
  formula,
  B = 200,
  method = "boot",
  remove_na = TRUE,
  plot = TRUE,
  plot_args = list(),
  ...
)
```

## Arguments

- data:

  A data frame containing outcome and predictors.

- formula:

  A logistic model formula (e.g., `status ~ age + sex`).

- B:

  Integer. Number of bootstrap resamples (default 200).

- method:

  Calibration method passed to
  [`rms::calibrate`](https://rdrr.io/pkg/rms/man/calibrate.html)
  (default "boot").

- remove_na:

  Logical; whether to drop rows with missing values.

- plot:

  Logical; whether to draw calibration plot.

- plot_args:

  List of additional arguments passed to
  [`plot()`](https://rdrr.io/r/graphics/plot.default.html).

- ...:

  Additional arguments passed to
  [`rms::lrm`](https://rdrr.io/pkg/rms/man/lrm.html).

## Value

A list with \`model\` (lrm), \`calibration\` (calibrate object), and
\`plot\` (recorded base plot if \`plot = TRUE\`).
