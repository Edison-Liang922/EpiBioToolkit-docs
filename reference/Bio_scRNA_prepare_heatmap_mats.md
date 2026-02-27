# Prepare logFC and p-value matrices for heatmap

Prepare logFC and p-value matrices for heatmap

## Usage

``` r
Bio_scRNA_prepare_heatmap_mats(
  markers_df,
  gene_col = "gene",
  celltype_col = "celltype",
  logfc_col = "avg_log2FC",
  p_col = "p_val",
  fill_logfc = 0,
  fill_p = 1
)
```

## Arguments

- markers_df:

  Data frame with gene, celltype, avg_log2FC, and p_val columns.

- gene_col:

  Column name for gene.

- celltype_col:

  Column name for cell type.

- logfc_col:

  Column name for logFC.

- p_col:

  Column name for p-value.

- fill_logfc:

  Value to fill missing logFC (default 0).

- fill_p:

  Value to fill missing p-values (default 1).

## Value

A list with logfc and pval matrices.
