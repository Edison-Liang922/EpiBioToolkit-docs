# Differential expression by cell type and condition

Differential expression by cell type and condition

## Usage

``` r
Bio_scRNA_de_by_celltype(
  object,
  condition_col = "orig.ident",
  celltype_col = "celltype",
  group_1,
  group_2,
  features = NULL,
  min_cells = 3,
  logfc_threshold = 0.25,
  ...
)
```

## Arguments

- object:

  A Seurat object.

- condition_col:

  Metadata column for condition (e.g., "orig.ident").

- celltype_col:

  Metadata column for cell type.

- group_1:

  Condition name for case group.

- group_2:

  Condition name for control group.

- features:

  Optional character vector of genes to test.

- min_cells:

  Minimum cells per group.

- logfc_threshold:

  Log fold-change threshold.

- ...:

  Additional arguments passed to Seurat::FindMarkers.

## Value

A list with markers, combined table, and diagnostics.
