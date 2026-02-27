# Create OTTERS stage 2 testing scripts

Generate bash scripts for OTTERS stage 2 (testing) and a \`run_me.sh\`
launcher script.

## Usage

``` r
Bio_OTTERS_create_sh_stage2(
  gwas_file,
  train_dir,
  anno_file,
  out_dir,
  nthread,
  model = "P0.001,P0.05,lassosum,SDPR,PRScs",
  name_by = "gwas",
  train_file_only = FALSE,
  env_file = "~/.otters_env",
  parallel = TRUE,
  print = FALSE,
  cl = NULL
)
```

## Arguments

- gwas_file:

  Character vector. GWAS summary files used for testing.

- train_dir:

  Character vector or scalar. Training output directory.

- anno_file:

  Character vector or scalar. Annotation file path(s).

- out_dir:

  Character vector or scalar. Base output directory.

- nthread:

  Integer. Number of threads for OTTERS.

- model:

  Character. Comma-separated models string for OTTERS.

- name_by:

  Character. One of `"gwas"`, `"train"`, or any string used as folder
  name.

- train_file_only:

  Logical. If TRUE, do not append `"Results_chr"` to `train_dir`.

- env_file:

  Character. Path to OTTERS environment config file. The file should
  have at least 4 rows: OTTERS_DIR, SDPR_DIR, Exp_geno_chr, PATH (one
  per row).

- parallel:

  Logical. If TRUE, \`run_me.sh\` joins commands with \`&\`.

- print:

  保留参数，暂不使用。

- cl:

  保留参数，暂不使用。

## Value

A list with:

- \`code_files\`: vector of generated \`stage2.sh\` paths.

- \`run_files\`: vector of generated \`run_me.sh\` paths.

## Details

Stage 2 is used to perform TWAS testing with trained weights. Here
\`gwas_file\` should be GWAS summary statistics, and \`train_dir\`
should point to the Stage 1 output directory (containing
\`Results_chr\*\`).

Output structure (per input GWAS file, depending on \`name_by\`):

- \`out_dir/basename(gwas_file)/code_temp/stage2.sh\` (name_by = "gwas")

- \`out_dir/basename(train_dir)/code_temp/stage2.sh\` (name_by =
  "train")

A \`run_me.sh\` is written to each \`out_dir\` base. When
\`train_file_only = FALSE\`, the script uses \`train_dir/Results_chr\`
as the weight directory.

The \`env_file\` is a plain text file with at least 4 rows (one per
line):


    /path/to/OTTERS
    /path/to/SDPR
    /path/to/geno/chr_prefix
    /path/to/conda/bin

These are exported into the script as OTTERS_DIR, SDPR_DIR,
Exp_geno_chr, and PATH (prefix), respectively.

## See also

\[Bio_OTTERS_create_sh()\], \[Bio_OTTERS_create_sh_stage1()\]
