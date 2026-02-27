# Extract Module Genes From WGCNA Results

Extract Module Genes From WGCNA Results

## Usage

``` r
Bio_Bulk_WGCNA_get_module_genes(wgcna_res, module_color)
```

## Arguments

- wgcna_res:

  Result object returned by \`Bio_Bulk_WGCNA\`, containing
  \`moduleColors\` and \`datExpr\`.

- module_color:

  Module color name (e.g., "turquoise").

## Value

A character vector of gene names.
