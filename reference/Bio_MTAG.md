# MTAG workflow (format + run)

Format GWAS summary statistics for MTAG and run mtag.py.

## Usage

``` r
Bio_MTAG(
  files,
  out_dir,
  n,
  col_map = list(snpid = "variant_id", chr = "chromosome", bp = "base_pair_location", a1
    = "effect_allele", a2 = "other_allele", freq = "effect_allele_frequency", beta =
    "beta", se = "standard_error", pval = "p_value"),
  format = TRUE,
  python_path = "/data/zhou-qtl/miniconda/envs/MTAG/bin/python",
  mtag_script = "/data/zhou-qtl/MTAG/mtag/mtag.py",
  base_file = NULL,
  extra_args = "--n_min 0.0 --stream_stdout --force"
)
```

## Arguments

- files:

  Character vector. Input GWAS file paths.

- out_dir:

  Character. Output directory.

- n:

  Numeric or numeric vector. Sample size(s) to attach.

- col_map:

  Named list of column mappings for MTAG formatting: snpid, chr, bp, a1,
  a2, freq, beta, se, pval.

- format:

  Logical. Whether to format input files into MTAG format.

- python_path:

  Character. Path to Python in the MTAG conda env.

- mtag_script:

  Character. Path to mtag.py.

- base_file:

  Character. If provided, run MTAG with base_file vs each formatted file
  in `files`. If NULL and `length(files) == 2`, run one MTAG job with
  both files.

- extra_args:

  Character. Extra arguments passed to mtag.py.

## Value

A list with formatted files and MTAG output prefixes.
