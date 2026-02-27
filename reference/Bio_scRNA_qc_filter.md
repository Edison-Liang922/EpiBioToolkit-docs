# QC filtering for scRNA-seq Seurat objects

Add mitochondrial (and optional ribosomal) percentage, optionally join
layers, and filter cells by standard QC thresholds.

## Usage

``` r
Bio_scRNA_qc_filter(
  object,
  mt_pattern = "^mt",
  calc_ribo = FALSE,
  ribo_pattern = "^Rpl|^Rps",
  min_features = 300,
  max_features = 4000,
  max_mt = 20,
  max_counts = 30000,
  join_layers = TRUE,
  return_counts = FALSE,
  assay = NULL,
  layer = "counts",
  slot = "counts"
)
```

## Arguments

- object:

  A Seurat object.

- mt_pattern:

  Regex pattern for mitochondrial genes (default "^mt").

- calc_ribo:

  Logical; compute percent.ribo if TRUE.

- ribo_pattern:

  Regex pattern for ribosomal genes (default "^Rpl\|^Rps").

- min_features:

  Minimum nFeature_RNA (NULL to skip).

- max_features:

  Maximum nFeature_RNA (NULL to skip).

- max_mt:

  Maximum percent.mt (NULL to skip).

- max_counts:

  Maximum nCount_RNA (NULL to skip).

- join_layers:

  Logical; call JoinLayers if available (Seurat v5).

- return_counts:

  Logical; return counts matrix in the result.

- assay:

  Assay name to use (NULL uses DefaultAssay).

- layer:

  Layer name for Seurat v5 (default "counts").

- slot:

  Slot name for Seurat v4 (default "counts").

## Value

If return_counts = FALSE, a filtered Seurat object. Otherwise, a list
with elements: object and counts.
