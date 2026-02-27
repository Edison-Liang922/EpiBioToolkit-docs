# Dimensionality plot wrapper

Dimensionality plot wrapper

## Usage

``` r
plot_scRNA_dim(object, reduction = "umap", group_by = NULL, label = TRUE, ...)
```

## Arguments

- object:

  A Seurat object.

- reduction:

  Reduction name (e.g., "umap", "tsne").

- group_by:

  Metadata column to color.

- label:

  Logical; show labels.

- ...:

  Additional arguments passed to Seurat::DimPlot.

## Value

A ggplot object.
