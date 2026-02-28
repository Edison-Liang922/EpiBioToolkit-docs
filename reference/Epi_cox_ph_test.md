# Cox PH Assumption Test

Test proportional hazards (PH) assumption using
[`survival::cox.zph`](https://rdrr.io/pkg/survival/man/cox.zph.html).

## Usage

``` r
Epi_cox_ph_test(
  cox_model,
  transform = "km",
  include_global = TRUE,
  pvalue_accuracy = 0.001
)
```

## Arguments

- cox_model:

  A fitted
  [`survival::coxph`](https://rdrr.io/pkg/survival/man/coxph.html)
  object.

- transform:

  Transform used in `cox.zph` (default "km").

- include_global:

  Logical; keep the GLOBAL row if present.

- pvalue_accuracy:

  Accuracy for p-value formatting (if \`scales\` available).

## Value

A list with \`table\` (data.frame) and \`ph_test\` (cox.zph object).
