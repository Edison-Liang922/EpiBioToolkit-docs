# One-click pipeline: single-sample CellChat

One-click pipeline: single-sample CellChat

## Usage

``` r
Bio_CellChat_pipeline_single(
  seu,
  group.by = "cell_type",
  sample.name = "Tumor",
  species = "human",
  db.category = "Secreted Signaling",
  assay = NULL,
  ppi.use = NULL,
  do.smooth = TRUE,
  population.size = TRUE,
  min.cells = 10,
  nboot = 100,
  seed.use = 1234,
  raw.use = TRUE,
  outdir = "cellchat_single",
  do.plot = TRUE,
  top.pathways = 20,
  signaling.to.plot = NULL,
  layout = "circle"
)
```

## Arguments

- seu:

  Seurat object.

- group.by:

  Character. Metadata column for cell identity.

- sample.name:

  Character. Sample label.

- species:

  Character. "human" or "mouse".

- db.category:

  Character. CellChat DB category.

- assay:

  Character. Seurat assay.

- ppi.use:

  PPI network to use (optional).

- do.smooth:

  Logical. Whether to run \codesmoothData.

- population.size:

  Logical. Use population size in \codecomputeCommunProb.

- min.cells:

  Integer. Minimum cells for interaction filtering.

- nboot:

  Integer. Bootstraps.

- seed.use:

  Integer. Random seed in CellChat.

- raw.use:

  Logical. Use raw data for \codecomputeCommunProb.

- outdir:

  Character. Output directory.

- do.plot:

  Logical. Generate plots.

- top.pathways:

  Integer. Top pathways to plot.

- signaling.to.plot:

  Character vector. Specific pathways to plot.

- layout:

  Character. Layout for pathway plots.

## Value

Invisibly, a list with CellChat results.
