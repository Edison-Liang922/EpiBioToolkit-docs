# Build Diagnostic Model With Nomogram and DCA

Build a multigene logistic model, generate a nomogram and DCA plot.

## Usage

``` r
Bio_build_diagnostic_model(
  expr,
  group_df,
  target_genes,
  project_name = "Combined_Model",
  sample_col = NULL,
  group_col = "group",
  case_label = "Case"
)
```

## Arguments

- expr:

  Expression matrix (genes x samples). Row names are gene IDs and column
  names are sample IDs.

- group_df:

  Sample metadata with sample IDs and group labels.

- target_genes:

  Target gene vector.

- project_name:

  Project name for output files.

- sample_col:

  Optional column in \`group_df\` for sample IDs. If \`NULL\`, row names
  of \`group_df\` are used.

- group_col:

  Column in \`group_df\` with group labels.

- case_label:

  Case label used as positive class.

## Value

A list with model object, DCA data, and plot.
