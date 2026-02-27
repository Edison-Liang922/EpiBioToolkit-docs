# Normalize, find variable features, scale, and run PCA

A fast preprocessing workflow for scRNA-seq Seurat objects.

## Usage

``` r
Bio_scRNA_normalize_pca(
  object,
  nfeatures = 2000,
  npcs = 50,
  regress_vars = NULL,
  ...
)
```

## Arguments

- object:

  A Seurat object.

- nfeatures:

  Number of variable features to select.

- npcs:

  Number of PCs to compute.

- regress_vars:

  Optional variables to regress in ScaleData.

- ...:

  Additional arguments passed to
  Seurat::NormalizeData/FindVariableFeatures/ScaleData/RunPCA.

## Value

A Seurat object with variable features and PCA computed.
