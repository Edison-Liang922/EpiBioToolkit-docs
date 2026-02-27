# Run UMAP and tSNE

Run UMAP and tSNE

## Usage

``` r
Bio_scRNA_run_umap_tsne(
  object,
  reduction = "harmony",
  dims = 1:30,
  run_umap = TRUE,
  run_tsne = TRUE,
  seed = 123,
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

- run_umap:

  Logical; run UMAP if TRUE.

- run_tsne:

  Logical; run tSNE if TRUE.

- seed:

  Random seed for embedding.

- ...:

  Additional arguments passed to RunUMAP/RunTSNE.

## Value

A Seurat object with UMAP/TSNE reductions.
