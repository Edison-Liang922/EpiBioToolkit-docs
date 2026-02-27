# WGCNA Analysis for Bulk RNA-seq

Run a standard WGCNA workflow and return key outputs for downstream
plotting.

## Usage

``` r
Bio_Bulk_WGCNA(
  expr,
  group,
  group_col = "group",
  sample_col = NULL,
  output_prefix = "WGCNA_Results",
  r_squared_cutoff = 0.85,
  mergeCutHeight = 0.25,
  nThreads = NULL,
  case_name = "Case",
  control_name = "Control",
  minModuleSize = 50,
  networkType = "unsigned",
  corType = "pearson",
  TOMType = "signed",
  power_vector = 1:30,
  maxBlockSize = NULL,
  remove_outliers = TRUE,
  outlier_cut_height = 300,
  outlier_min_size = 10
)
```

## Arguments

- expr:

  Expression matrix/data frame. Samples can be in rows or columns.
  Row/column names should be sample IDs and gene IDs.

- group:

  Sample metadata with sample IDs and a grouping column.

- group_col:

  Column name in \`group\` for case/control labels.

- sample_col:

  Optional column name in \`group\` for sample IDs. If \`NULL\`, row
  names of \`group\` are used.

- output_prefix:

  Prefix string stored in the output list.

- r_squared_cutoff:

  Soft-threshold R^2 target for picking power.

- mergeCutHeight:

  Module merge threshold.

- nThreads:

  Number of threads for WGCNA (NULL uses default).

- case_name:

  Case label in \`group_col\`.

- control_name:

  Control label in \`group_col\`.

- minModuleSize:

  Minimum number of genes per module.

- networkType:

  Network type for adjacency (e.g., "unsigned", "signed").

- corType:

  Correlation type (e.g., "pearson", "bicor").

- TOMType:

  TOM type (e.g., "signed", "unsigned").

- power_vector:

  Candidate powers for soft-threshold selection.

- maxBlockSize:

  Max block size for \`blockwiseModules\`.

- remove_outliers:

  Logical; whether to remove outlier samples.

- outlier_cut_height:

  Cut height for sample clustering.

- outlier_min_size:

  Minimum cluster size for outlier removal.

## Value

A list with key WGCNA outputs (modules, eigengenes, correlations).
