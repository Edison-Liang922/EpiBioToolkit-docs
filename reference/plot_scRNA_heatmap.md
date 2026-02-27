# Heatmap of logFC with p-value stars

Heatmap of logFC with p-value stars

## Usage

``` r
plot_scRNA_heatmap(
  logfc_mat,
  p_mat = NULL,
  p_cut1 = 0.05,
  p_cut2 = 0.01,
  color_low = "#1D74E7",
  color_mid = "white",
  color_high = "red2",
  ...
)
```

## Arguments

- logfc_mat:

  Numeric matrix/data.frame (genes x cell types).

- p_mat:

  Optional p-value matrix/data.frame (same shape as logfc_mat).

- p_cut1:

  P-value cutoff for "\*" (default 0.05).

- p_cut2:

  P-value cutoff for "\*\*" (default 0.01).

- color_low:

  Low color.

- color_mid:

  Mid color.

- color_high:

  High color.

- ...:

  Additional arguments passed to pheatmap::pheatmap.

## Value

A pheatmap object.
