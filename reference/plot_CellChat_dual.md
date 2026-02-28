# CellChat plots for dual sample comparison

CellChat plots for dual sample comparison

## Usage

``` r
plot_CellChat_dual(
  cellchat.merged,
  cellchat.list = NULL,
  outdir = "cellchat_dual_plots",
  prefix = "dual",
  group.colors = c("#E95C59", "#476D87", "#E39A35", "#3AA17E"),
  comparison = c(1, 2),
  sources.use = NULL,
  targets.use = NULL,
  width = 10,
  height = 7
)
```

## Arguments

- cellchat.merged:

  Merged CellChat object.

- cellchat.list:

  List of per-group CellChat objects (optional).

- outdir:

  Character. Output directory.

- prefix:

  Character. File prefix.

- group.colors:

  Character vector. Colors for comparison.

- comparison:

  Integer vector. Which group indices to compare.

- sources.use:

  Character vector. Source cell types.

- targets.use:

  Character vector. Target cell types.

- width:

  Numeric. Plot width.

- height:

  Numeric. Plot height.

## Value

Invisibly, output directory.
