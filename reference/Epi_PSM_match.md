# Propensity Score Matching (PSM)

Generic PSM wrapper using MatchIt. Returns matched data for downstream
analysis.

## Usage

``` r
Epi_PSM_match(
  data,
  treat_col,
  covariates,
  case_label = NULL,
  control_label = NULL,
  method = "nearest",
  distance = "glm",
  ratio = 1,
  caliper = 0.1,
  replace = FALSE,
  return_model = FALSE,
  ...
)
```

## Arguments

- data:

  A data frame containing treatment/exposure and covariates.

- treat_col:

  Column name for treatment/exposure variable (binary). This can be 0/1,
  two unique numeric values, or two category labels.

- covariates:

  Character vector of covariate column names used to estimate the
  propensity score.

- case_label:

  Optional value in \`treat_col\` representing the treated group (mapped
  to 1). Required if \`treat_col\` is categorical and you want explicit
  control/treated labels.

- control_label:

  Optional value in \`treat_col\` representing the control group (mapped
  to 0).

- method:

  Matching method (default: \`"nearest"\`).

- distance:

  Distance model (default: \`"glm"\`).

- ratio:

  Matching ratio (default: 1).

- caliper:

  Caliper width (default: 0.1).

- replace:

  Whether to match with replacement (default: \`FALSE\`).

- return_model:

  Logical; return the \`matchit\` object as well.

- ...:

  Additional arguments passed to \`MatchIt::matchit\`.

## Value

If \`return_model = FALSE\`, a matched data frame. Otherwise a list with
\`matched_data\` and \`matchit_model\`.
