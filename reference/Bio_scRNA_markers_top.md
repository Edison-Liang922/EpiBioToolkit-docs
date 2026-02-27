# Find markers and top genes per cluster

Find markers and top genes per cluster

## Usage

``` r
Bio_scRNA_markers_top(
  object,
  only_pos = TRUE,
  min_pct = 0.25,
  logfc_threshold = 0.25,
  adj_p_cut = 0.05,
  top_n = 50,
  ...
)
```

## Arguments

- object:

  A Seurat object.

- only_pos:

  Logical; find only positive markers.

- min_pct:

  Minimum fraction of cells expressing the gene.

- logfc_threshold:

  Log fold-change threshold.

- adj_p_cut:

  Adjusted p-value cutoff for filtering.

- top_n:

  Top genes per cluster to keep.

- ...:

  Additional arguments passed to Seurat::FindAllMarkers.

## Value

A list with all_markers, filtered, and top lists.
