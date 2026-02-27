# QC violin plot for scRNA-seq

QC violin plot for scRNA-seq

## Usage

``` r
plot_scRNA_qc_violin(
  object,
  features = c("nFeature_RNA", "nCount_RNA", "percent.mt"),
  ...
)
```

## Arguments

- object:

  A Seurat object.

- features:

  QC features to plot.

- ...:

  Additional arguments passed to Seurat::VlnPlot.

## Value

A ggplot object.
