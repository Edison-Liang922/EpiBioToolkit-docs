# Time-dependent ROC for Survival Outcomes

Compute time-dependent ROC curves using
[`timeROC::timeROC`](https://rdrr.io/pkg/timeROC/man/timeROC.html).

## Usage

``` r
Epi_timeROC(
  data,
  time_col,
  status_col,
  marker_col,
  times,
  event_label = NULL,
  censor_label = NULL,
  remove_na = TRUE,
  cause = 1,
  weighting = "marginal",
  iid = TRUE,
  ...
)
```

## Arguments

- data:

  A data frame containing time, status, and marker.

- time_col:

  Column name for survival time.

- status_col:

  Column name for event status (1 = event, 0 = censored).

- marker_col:

  Column name for risk score/marker.

- times:

  Numeric vector of time points for ROC.

- event_label:

  Optional value in \`status_col\` mapped to 1.

- censor_label:

  Optional value in \`status_col\` mapped to 0.

- remove_na:

  Logical; whether to drop rows with missing values.

- cause:

  Integer event of interest (default 1).

- weighting:

  Weighting method for `timeROC` (default "marginal").

- iid:

  Logical; compute influence function (default TRUE).

- ...:

  Additional arguments passed to
  [`timeROC::timeROC`](https://rdrr.io/pkg/timeROC/man/timeROC.html).

## Value

A list with \`timeROC\` object and \`auc_table\`.
