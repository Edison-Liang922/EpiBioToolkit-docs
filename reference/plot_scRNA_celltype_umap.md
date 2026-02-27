# Cluster tree plot for resolution sweep

Cluster tree plot for resolution sweep

## Usage

``` r
plot_scRNA_celltype_umap(
  object,
  reduction = "umap",
  celltype_col = "celltype",
  palette = NULL,
  point_size = 1.2,
  alpha = 0.5,
  label = TRUE,
  label_size = 4
)
```

## Arguments

- object:

  A Seurat object.

- reduction:

  Reduction name (default "umap").

- celltype_col:

  Metadata column for cell type.

- palette:

  Optional named vector of colors.

- point_size:

  Point size.

- alpha:

  Point alpha.

- label:

  Logical; add text labels.

- label_size:

  Label size.

- prefix:

  Prefix used for clustering columns (default \\RNA_snn_res.\\).#'
  @param flip Logical; flip coordinates for readability.#'#' @return A
  ggplot object.#' @export#'\_scRNA_clustree \<- function(object, prefix
  = \\RNA_snn_res.\\, flip = TRUE) if (!requireNamespace(\\clustree\\,
  quietly = TRUE)) stop(\\Package 'clustree' is required.\\) if
  (!requireNamespace(\\ggplot2\\, quietly = TRUE)) stop(\\Package
  'ggplot2' is required.\\) p \<- clustree::clustree(object, prefix =
  prefix) if (isTRUE(flip)) p \<- p + ggplot2::coord_flip() p+ \#' UMAP
  with median labels per cell type UMAP with median labels per cell type

## Value

A ggplot object.
