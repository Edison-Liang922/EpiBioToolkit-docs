# Demo parameters for scTWAS script generation

Example input list for `Bio_scTWAS_create_sh`.

## Usage

``` r
sc_twas_demo
```

## Format

A list with:

- name_or_db:

  NULL, meaning all `.db` files in `weights_dir` are used.

- trait:

  Trait label used in output file names.

- weights_dir:

  Directory containing model `.db` files.

- out_dir:

  Output directory for scripts and results.

- spredixcan_path:

  Path to `SPrediXcan.py`.

- gwas_file:

  GWAS summary file path.

- parallel:

  Whether run_me.sh runs jobs in parallel.

## Source

Simulated example for documentation and testing.
