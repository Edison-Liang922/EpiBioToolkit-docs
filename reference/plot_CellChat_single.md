# CellChat plots for single sample

CellChat plots for single sample

## Usage

``` r
plot_CellChat_single(
  cellchat,
  outdir = "cellchat_single_plots",
  prefix = "single",
  top.pathways = 20,
  signaling.to.plot = NULL,
  layout = c("circle", "hierarchy", "chord"),
  width = 9,
  height = 7
)
```

## Arguments

- cellchat:

  A CellChat object.

- outdir:

  Character. Output directory.

- prefix:

  Character. File prefix.

- top.pathways:

  Integer. Top pathways to plot.

- signaling.to.plot:

  Character vector. Specific pathways to plot.

- layout:

  Character. Layout for pathway plots: "circle", "hierarchy", or
  "chord".

- width:

  Numeric. Plot width.

- height:

  Numeric. Plot height.

## Value

Invisibly, output directory.
