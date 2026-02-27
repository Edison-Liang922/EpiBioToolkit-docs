# Colocalization Analysis for eQTL and Outcome Data

Standardizes input columns, applies optional cis-window filtering, and
runs \`coloc::coloc.abf\` per gene to summarize posterior probabilities.

## Usage

``` r
Bio_coloc(
  expo,
  outcome,
  result_file_path = NULL,
  window = 1e+06,
  p1 = 1e-04,
  p2 = 1e-04,
  p12 = 1e-05,
  outcome_type = "cc",
  expo_type = "quant"
)
```

## Arguments

- expo:

  A data frame of exposure (eQTL) summary statistics. Either provide
  standardized columns: \`snp\` (variant ID), \`pval\` (P-value),
  \`beta\` (effect), \`varbeta\` (SE^2), \`pos\` (base-pair position),
  \`maf\` (minor allele frequency), \`N\` (sample size),
  \`gene.exposure\` (gene ID), and optional \`Probe_bp\` (gene
  position); or raw columns: \`SNP\`, \`p\`, \`b\`, \`SE\`, \`Freq\`,
  \`BP\`, \`n\`, \`Gene\`, and \`Probe_bp\` for cis-window filtering.

- outcome:

  A data frame of outcome (GWAS) summary statistics. Either provide
  standardized columns: \`snp\` (variant ID), \`pval\` (P-value),
  \`beta\` (effect), \`varbeta\` (SE^2), \`pos\` (base-pair position),
  \`maf\` (minor allele frequency); or raw columns: \`SNP\`, \`P\`,
  \`BETA\`, \`SE\`, \`POS\`, \`EAF\` (effect allele frequency).

- result_file_path:

  Optional file path to write a CSV summary.

- window:

  Numeric window size for cis filtering around \`Probe_bp\`. Set to
  \`NULL\` to skip cis filtering. Default is \`1e6\`.

- p1:

  Prior probability for trait 1. Default is \`1e-4\`.

- p2:

  Prior probability for trait 2. Default is \`1e-4\`.

- p12:

  Prior probability for colocalization. Default is \`1e-5\`.

- outcome_type:

  Outcome trait type for coloc (e.g., \`"cc"\` or \`"quant"\`).

- expo_type:

  Exposure trait type for coloc (e.g., \`"quant"\`).

## Value

A data frame with gene-level colocalization summaries: \`gene\`,
\`nsnp\`, and \`PP.H0.abf\` to \`PP.H4.abf\`. Genes with fewer than 2
overlapping SNPs are skipped.
