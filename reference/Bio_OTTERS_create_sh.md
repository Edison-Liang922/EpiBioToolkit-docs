# Create OTTERS scripts (stage 1 or stage 2)

Wrapper function to generate OTTERS stage 1 (training) or stage 2
(testing) scripts. Internally calls `Bio_OTTERS_create_sh_stage1` or
`Bio_OTTERS_create_sh_stage2` based on `stage`.

## Usage

``` r
Bio_OTTERS_create_sh(
  stage = 2,
  gwas_file,
  anno_file,
  out_dir,
  nthread,
  model = "P0.001,P0.05,lassosum,SDPR,PRScs",
  env_file = "~/.otters_env",
  parallel = TRUE,
  train_dir = NULL,
  name_by = "gwas",
  train_file_only = FALSE,
  print = FALSE,
  cl = NULL
)
```

## Arguments

- stage:

  Integer. 1 for training, 2 for testing.

- gwas_file:

  Character vector. Summary statistics files used for the selected stage
  (Stage 1: eQTL summary; Stage 2: GWAS summary).

- anno_file:

  Character vector or scalar. OTTERS annotation file path(s).

- out_dir:

  Character vector or scalar. Base output directory.

- nthread:

  Integer. Number of threads for OTTERS.

- model:

  Character. Comma-separated models string for OTTERS. Recommended:

  - Stage 1: `"PT,lassosum,PRScs,SDPR"`

  - Stage 2: `"P0.001,P0.05,lassosum,SDPR,PRScs"`

- env_file:

  Character. Path to OTTERS environment config file.

- parallel:

  Logical. Whether to join commands with \`&\` in \`run_me.sh\`.

- train_dir:

  Character vector or scalar. Training output directory (stage 2 only).

- name_by:

  Character. One of `"gwas"`, `"train"`, or any string used as folder
  name (stage 2 only).

- train_file_only:

  Logical. If TRUE, do not append `"Results_chr"` to `train_dir` (stage
  2 only).

- print:

  保留参数，暂不使用。

- cl:

  保留参数，暂不使用。

## Value

A list with \`code_files\` and \`run_files\` created.

## Details

Stage 1 is used to train weights (typically eQTL weights). The input
\`gwas_file\` should be the summary statistics used for training
(commonly eQTL summary stats), and \`anno_file\` should be the OTTERS
annotation file (e.g., \*\_hg38_anno.txt from `Bio_OTTERS_format_eqtl`).

Stage 2 is used to perform TWAS testing with trained weights. The input
\`gwas_file\` should be GWAS summary statistics, and \`train_dir\`
should point to the Stage 1 output directory (containing
\`Results_chr\*\`).

The \`env_file\` is a plain text file with at least 4 rows (one per
line):


    /path/to/OTTERS
    /path/to/SDPR
    /path/to/geno/chr_prefix
    /path/to/conda/bin

## See also

\[Bio_OTTERS_create_sh_stage1()\], \[Bio_OTTERS_create_sh_stage2()\]
