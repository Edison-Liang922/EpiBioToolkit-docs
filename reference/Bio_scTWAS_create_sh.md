# Create SPrediXcan (scTWAS) shell scripts

Generate shell scripts to run SPrediXcan for one or more model
databases.

## Usage

``` r
Bio_scTWAS_create_sh(
  name_or_db = NULL,
  trait = "AP",
  weights_dir = "/data/s01005/Data/scTWAS",
  out_dir = "/data/s01005/Data/MAFLD/scTWAS",
  spredixcan_path = "/home/a3v2s01005/MetaXcan-master/software/SPrediXcan.py",
  gwas_file = "/data/s01005/Data/MAFLD/GWAS_prossess.txt.gz",
  pattern = "\\.db$",
  check_exists = TRUE,
  keep_non_rsid = TRUE,
  additional_output = TRUE,
  model_db_snp_key = "varID",
  throw = TRUE,
  snp_column = "panel_variant_id",
  effect_allele_column = "effect_allele",
  non_effect_allele_column = "non_effect_allele",
  beta_column = "effect_size",
  zscore_column = "zscore",
  pvalue_column = "pvalue",
  run_me = TRUE,
  parallel = TRUE
)
```

## Arguments

- name_or_db:

  Character vector. Model name(s) or .db path(s). If NULL, all .db files
  under `weights_dir` are used.

- trait:

  Character. Trait name used in output file naming.

- weights_dir:

  Character. Directory containing model .db and covariance files. Used
  when `name_or_db` is model name(s).

- out_dir:

  Character. Output directory for results and scripts.

- spredixcan_path:

  Character. Path to SPrediXcan.py.

- gwas_file:

  Character. GWAS file path.

- pattern:

  Character. Regex pattern for model db files when scanning
  `weights_dir`. Default matches `.db`.

- check_exists:

  Logical. If TRUE, warn when model/cov files are missing.

- keep_non_rsid:

  Logical. Whether to pass `--keep_non_rsid`.

- additional_output:

  Logical. Whether to pass `--additional_output`.

- model_db_snp_key:

  Character. `--model_db_snp_key` value.

- throw:

  Logical. Whether to pass `--throw`.

- snp_column:

  Character. GWAS SNP column name.

- effect_allele_column:

  Character. Effect allele column name.

- non_effect_allele_column:

  Character. Non-effect allele column name.

- beta_column:

  Character. Beta column name.

- zscore_column:

  Character. Z-score column name.

- pvalue_column:

  Character. P-value column name.

- run_me:

  Logical. Whether to create a `run_me.sh`.

- parallel:

  Logical. If TRUE, join run commands with `&`.

## Value

A list with:

- `scripts`: vector of script paths.

- `run_file`: path to run script (if created).

- `models`: resolved model db paths.

## Details

The function resolves a model `.db` file and its covariance file
`*_covariances.txt.gz`. If `name_or_db = NULL`, all `.db` files under
`weights_dir` are used. Each model generates a standalone shell script,
and an optional `run_me.sh` is written to `out_dir`.
