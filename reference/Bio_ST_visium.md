# Visium spatial transcriptomics pipeline (Python/Scanpy)

Run a Scanpy-based Visium workflow via \codesystem2(). The Python script
lives in \codeinst/python/st_visium_pipeline.py.

## Usage

``` r
Bio_ST_visium(
  input_dir,
  count_file = "filtered_feature_bc_matrix.h5",
  out_dir = input_dir,
  prefix = NULL,
  python_path = "python3",
  annotation_map = NULL,
  min_counts = 500,
  max_counts = 20000,
  max_pct_mt = 20,
  max_pct_hb = 3,
  max_pct_plat = 1,
  n_top_genes = 2000,
  n_neighbors = 20,
  n_pcs = 10,
  resolution = 0.8,
  n_iterations = 10,
  umap_min_dist = 0.3,
  markers_top_n = 50,
  pval_cutoff = 0.05,
  seed = 0,
  save_plots = FALSE,
  plot_format = "png",
  img_key = "hires",
  spot_size = 1.5,
  alpha = 0.8,
  out_h5ad = NULL,
  script_path = NULL,
  extra_args = NULL,
  verbose = TRUE
)
```

## Arguments

- input_dir:

  Character. Visium input folder (10X output directory).

- count_file:

  Character. Count file name inside \codeinput_dir.

- out_dir:

  Character. Output directory for results.

- prefix:

  Character. Output prefix (default: folder name of \codeinput_dir).

- python_path:

  Character. Python executable path or command.

- annotation_map:

  Character. CSV/TSV with columns: cluster, annotation.

- min_counts:

  Integer. Minimum total counts per spot.

- max_counts:

  Integer. Maximum total counts per spot.

- max_pct_mt:

  Numeric. Max mitochondrial percent.

- max_pct_hb:

  Numeric. Max hemoglobin percent.

- max_pct_plat:

  Numeric. Max platelet percent.

- n_top_genes:

  Integer. Number of highly variable genes.

- n_neighbors:

  Integer. Neighbors for graph construction.

- n_pcs:

  Integer. PCs used in neighbors.

- resolution:

  Numeric. Leiden resolution.

- n_iterations:

  Integer. Leiden iterations.

- umap_min_dist:

  Numeric. UMAP min_dist.

- markers_top_n:

  Integer. Top markers per cluster to export.

- pval_cutoff:

  Numeric. P-value cutoff for markers.

- seed:

  Integer. Random seed.

- save_plots:

  Logical. Save QC/UMAP/spatial plots.

- plot_format:

  Character. Plot file extension (e.g. \code"png").

- img_key:

  Character. Image key for Visium plots.

- spot_size:

  Numeric. Spot size for spatial plots.

- alpha:

  Numeric. Alpha for annotation spatial plots.

- out_h5ad:

  Character. Output h5ad path (optional).

- script_path:

  Character. Path to Python script (optional override).

- extra_args:

  Character vector. Extra CLI args passed to Python.

- verbose:

  Logical. Print Python output.

## Value

A list of output paths and the executed command.
