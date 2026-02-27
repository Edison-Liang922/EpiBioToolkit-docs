# Pick number of PCs based on variance heuristics

Compute cumulative variance and heuristic cutoffs to select PC
dimensions.

## Usage

``` r
Bio_scRNA_pick_dims(
  object,
  reduction = "harmony",
  cumu_cut = 90,
  pct_cut = 5,
  delta_cut = 0.1
)
```

## Arguments

- object:

  A Seurat object with a reduction (PCA/Harmony).

- reduction:

  Reduction name (default "harmony").

- cumu_cut:

  Cumulative variance cutoff (default 90).

- pct_cut:

  Single PC variance cutoff (default 5).

- delta_cut:

  Drop threshold for variance difference (default 0.1).

## Value

A list with pct, cumu, co1, co2, and pcs (selected dims).
