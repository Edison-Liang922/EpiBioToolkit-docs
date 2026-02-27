# Cell cycle scoring for scRNA-seq

Normalize data (optional) and compute S and G2M scores.

## Usage

``` r
Bio_scRNA_cellcycle_score(
  object,
  s_features = NULL,
  g2m_features = NULL,
  normalize = TRUE,
  ...
)
```

## Arguments

- object:

  A Seurat object.

- s_features:

  S phase gene vector. If NULL, uses Seurat::cc.genes\$s.genes.

- g2m_features:

  G2M phase gene vector. If NULL, uses Seurat::cc.genes\$g2m.genes.

- normalize:

  Logical; run NormalizeData first.

- ...:

  Additional arguments passed to Seurat::CellCycleScoring.

## Value

A Seurat object with S.Score, G2M.Score, and Phase.
