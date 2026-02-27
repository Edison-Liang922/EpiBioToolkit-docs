# SCTransform with optional integration

Run SCTransform on a Seurat object. If split_by is provided, perform SCT
integration across groups.

## Usage

``` r
Bio_scRNA_sctransform(
  object,
  split_by = NULL,
  regress_vars = c("percent.mt", "S.Score", "G2M.Score"),
  nfeatures = 3000,
  return_list = FALSE,
  ...
)
```

## Arguments

- object:

  A Seurat object.

- split_by:

  Metadata column used to split object for integration (NULL for no
  integration).

- regress_vars:

  Variables to regress in SCTransform.

- nfeatures:

  Number of integration features.

- return_list:

  Logical; if TRUE return a list with intermediate objects.

- ...:

  Additional arguments passed to Seurat::SCTransform.

## Value

A Seurat object, or a list when return_list = TRUE.
