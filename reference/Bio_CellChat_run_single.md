# Run CellChat for a single sample

Run CellChat for a single sample

## Usage

``` r
Bio_CellChat_run_single(
  seu,
  group.by = "cell_type",
  sample.name = "Tumor",
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
  outdir = "cellchat_single",
  save.rds = TRUE
)
```

## Arguments

- seu:

  Seurat object.

- group.by:

  Character. Metadata column for cell identity.

- sample.name:

  Character. Sample label for outputs.

- species:

  Character. "human" or "mouse".

- db.category:

  Character. CellChat DB category (default "Secreted Signaling").

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

  Logical. Save cellchat object.

## Value

A list with cellchat object and output paths.
