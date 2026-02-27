# Plot WGCNA Results

Generate standard WGCNA diagnostic plots from \`Bio_Bulk_WGCNA\` output.

## Usage

``` r
Bio_Bulk_plot_wgcna_results(wgcna_res, plot_outliers = TRUE)
```

## Arguments

- wgcna_res:

  Result object returned by \`Bio_Bulk_WGCNA\`, containing \`sft_data\`,
  \`net\`, \`moduleColors\`, \`datTraits_numeric\`, \`MEs\`,
  \`moduleTraitCor\`, \`moduleTraitPvalue\`, \`MM\`, \`GS\`, and
  \`prefix\`.

- plot_outliers:

  Logical; currently reserved for compatibility.

## Value

Invisibly returns \`TRUE\` after plotting.
