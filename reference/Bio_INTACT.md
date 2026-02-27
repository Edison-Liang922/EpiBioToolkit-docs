# INTACT Integration for Colocalization and TWAS

Compute INTACT posterior probabilities by combining colocalization GLCP
with TWAS z-scores.

## Usage

``` r
Bio_INTACT(
  coloc,
  twas,
  gene_col_coloc = "gene",
  gene_col_twas = "gene",
  h3_col = "PP.H3.abf",
  h4_col = "PP.H4.abf",
  z_col = "TWAS_z",
  p_col = NULL,
  prior_fun = INTACT::linear,
  sort = TRUE
)
```

## Arguments

- coloc:

  A data frame with colocalization summary results. Required columns:
  gene ID (\`gene_col_coloc\`), \`PP.H3.abf\` (posterior for H3) and
  \`PP.H4.abf\` (posterior for H4/colocalization).

- twas:

  A data frame with TWAS summary results. Required columns: gene ID
  (\`gene_col_twas\`) and z-score (\`z_col\`); optional P-value
  (\`p_col\`).

- gene_col_coloc:

  Column name for gene ID in \`coloc\`.

- gene_col_twas:

  Column name for gene ID in \`twas\`.

- h3_col:

  Column name for PP.H3.abf in \`coloc\`.

- h4_col:

  Column name for PP.H4.abf in \`coloc\`.

- z_col:

  Column name for TWAS z-scores in \`twas\`.

- p_col:

  Optional column name for TWAS P-values in \`twas\`.

- prior_fun:

  Prior function passed to \`INTACT::intact\` (default:
  \`INTACT::linear\`).

- sort:

  Logical; sort output by descending INTACT posterior.

## Value

A data frame with GLCP and INTACT posterior per gene.
