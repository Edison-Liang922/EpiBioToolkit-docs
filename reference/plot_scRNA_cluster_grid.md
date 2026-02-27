# Grid of UMAPs across clustering resolutions

Grid of UMAPs across clustering resolutions

## Usage

``` r
plot_scRNA_cluster_grid(
  object,
  reduction = "umap",
  prefix = "RNA_snn_res.",
  resolutions = seq(0.2, 0.8, by = 0.1),
  ncol = 3,
  label = TRUE
)
```

## Arguments

- object:

  A Seurat object.

- reduction:

  Reduction name (default "umap").

- prefix:

  Metadata prefix for clustering (default "RNA_snn_res.").

- resolutions:

  Numeric vector of resolutions.

- ncol:

  Number of columns in the grid.

- label:

  Logical; show cluster labels.

## Value

A patchwork plot.
