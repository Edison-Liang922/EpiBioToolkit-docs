# Run CellChat for two conditions

Run CellChat for two conditions

## Usage

``` r
Bio_CellChat_run_dual(
  seu,
  sample.group = "group",
  groups = c("Normal", "Tumor"),
  sample.names = NULL,
  group.by = "cell_type",
  species = c("human", "mouse"),
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
  save.rds = TRUE
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

  Character. Seurat assay to use.

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

- save.rds:

  Logical. Save cellchat objects.

## Value

A list with merged and per-group CellChat results.
