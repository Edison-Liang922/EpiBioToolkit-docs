# Run Harmony integration

Run Harmony integration

## Usage

``` r
Bio_scRNA_run_harmony(
  object,
  group_by = "orig.ident",
  reduction = "pca",
  dims = 1:50,
  ...
)
```

## Arguments

- object:

  A Seurat object with PCA computed.

- group_by:

  Metadata column(s) to regress (e.g., "orig.ident").

- reduction:

  Reduction to use as input (default "pca").

- dims:

  Dimensions to use.

- ...:

  Additional arguments passed to harmony::RunHarmony.

## Value

A Seurat object with Harmony reduction.
