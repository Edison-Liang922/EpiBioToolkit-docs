# CIBERSORT Immune Infiltration Analysis

Run CIBERSORT and prepare wide/long data for downstream visualization.

## Usage

``` r
Bio_Bulk_cibersort_analysis(
  expr,
  group_df,
  perm = 100,
  QN = FALSE,
  sample_col = NULL,
  group_col = "group",
  sig_matrix = NULL
)
```

## Arguments

- expr:

  Expression matrix/data frame with genes in rows and samples in
  columns. Row names are gene IDs and column names are sample IDs.

- group_df:

  Sample metadata with sample IDs and group labels.

- perm:

  Permutation number for CIBERSORT (e.g., 100 or 1000).

- QN:

  Quantile normalization. Use \`FALSE\` for RNA-seq, \`TRUE\` for
  microarray.

- sample_col:

  Optional column in \`group_df\` for sample IDs. If \`NULL\`, row names
  of \`group_df\` are used.

- group_col:

  Column in \`group_df\` with group labels.

- sig_matrix:

  Path to signature matrix file. If \`NULL\`, use LM22 from the
  \`CIBERSORT\` package extdata.

## Value

A list with:

- raw_results:

  Original CIBERSORT output (including P-value, RMSE).

- wide_data:

  Filtered wide matrix (samples x cell types).

- long_data:

  Long-format data with Sample/Group/CellType/Composition.
