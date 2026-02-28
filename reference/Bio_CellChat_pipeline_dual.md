# One-click pipeline: dual-sample CellChat

One-click pipeline: dual-sample CellChat

## Usage

``` r
Bio_CellChat_pipeline_dual(
  seu,
  sample.group = "group",
  groups = c("Normal", "Tumor"),
  sample.names = NULL,
  group.by = "cell_type",
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
  outdir = "cellchat_dual",
  do.plot = TRUE,
  group.colors = c("#E95C59", "#476D87", "#E39A35", "#3AA17E"),
  comparison = c(1, 2),
  sources.use = NULL,
  targets.use = NULL
)
```

## Arguments

- seu:

  Seurat object.

- sample.group:

  Character. Metadata column for sample grouping.

- groups:

  Character vector. Group labels to compare.

- sample.names:

  Character vector. Names for each group.

- group.by:

  Character. Metadata column for cell identity.

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

- group.colors:

  Character vector. Colors for comparisons.

- comparison:

  Integer vector. Comparison indices.

- sources.use:

  Character vector. Source cell types.

- targets.use:

  Character vector. Target cell types.

## Value

Invisibly, a list with CellChat results.
