# PSM Baseline Tables Before/After Matching

Create baseline characteristic tables (before and after matching) using
gtsummary.

## Usage

``` r
Epi_PSM_baseline_tables(
  data,
  treat_col,
  covariates,
  matched_data = NULL,
  matchit_model = NULL,
  labels = NULL,
  missing_text = "缺失",
  pvalue_fun = NULL,
  pvalue_accuracy = 0.001
)
```

## Arguments

- data:

  Original data frame containing treatment and covariates.

- treat_col:

  Column name for treatment/exposure variable.

- covariates:

  Character vector of covariate column names.

- matched_data:

  Optional matched data frame. If \`NULL\`, provide \`matchit_model\`.

- matchit_model:

  Optional MatchIt model object to derive matched data.

- labels:

  Optional named list to relabel variables in the table.

- missing_text:

  Text for missing values.

- pvalue_fun:

  Optional function for p-values (e.g., \`scales::pvalue\`).

- pvalue_accuracy:

  Accuracy for \`scales::pvalue\` (if used).

## Value

A list with \`before\` and \`after\` gtsummary tables.
