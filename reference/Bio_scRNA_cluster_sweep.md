# Cluster sweep across resolutions

Run neighbors and multiple resolutions of FindClusters.

## Usage

``` r
Bio_scRNA_cluster_sweep(
  object,
  reduction = "harmony",
  dims = 1:30,
  resolutions = seq(0.2, 0.8, by = 0.1),
  final_resolution = NULL,
  ...
)
```

## Arguments

- object:

  A Seurat object.

- reduction:

  Reduction to use (default "harmony").

- dims:

  Dimensions to use.

- resolutions:

  Numeric vector of resolutions.

- final_resolution:

  Optional final resolution to set as default.

- ...:

  Additional arguments passed to Seurat::FindClusters.

## Value

A Seurat object with clustering results stored in metadata.
