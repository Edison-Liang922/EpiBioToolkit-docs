# Assign cell types by cluster mapping

Assign cell types by cluster mapping

## Usage

``` r
Bio_scRNA_assign_celltype(
  object,
  mapping,
  cluster_col = "seurat_clusters",
  new_col = "celltype"
)
```

## Arguments

- object:

  A Seurat object.

- mapping:

  Named character vector with names = cluster IDs, values = cell types.

- cluster_col:

  Metadata column for clusters (NULL uses Idents).

- new_col:

  Name of the new metadata column.

## Value

A Seurat object with cell type annotations.
