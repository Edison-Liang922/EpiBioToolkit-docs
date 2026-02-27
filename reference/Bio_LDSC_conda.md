# Conda-based LDSC workflow (format + munge + rg)

Format GWAS summary statistics for LDSC, run munge_sumstats.py, and
optionally run ldsc.py genetic correlation.

## Usage

``` r
Bio_LDSC_conda(
  files,
  out_dir,
  n,
  col_map = list(snpid = "variant_id", a1 = "effect_allele", a2 = "other_allele", beta =
    "beta", se = "standard_error", chr = "chromosome", bp = "base_pair_location", pval =
    "p_value"),
  format = TRUE,
  python_path = "/data/zhou-qtl/miniconda/envs/ldsc/bin/python",
  munge_script = "/data/zhou-qtl/LDSC/ldsc/munge_sumstats.py",
  merge_alleles = "/data/zhou-qtl/LDSC/ldsc/w_hm3.snplist",
  chunksize = 500000L,
  run_rg = FALSE,
  rg_ref = NULL,
  ldsc_script = "/data/zhou-qtl/LDSC/ldsc/ldsc.py",
  ref_ld_chr = "/data/zhou-qtl/LDSC/LDfile/eur_w_ld_chr/",
  w_ld_chr = "/data/zhou-qtl/LDSC/LDfile/eur_w_ld_chr/",
  rg_out_dir = out_dir
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

  Named list of column mappings for LDSC formatting: snpid, a1, a2,
  beta, se, chr, bp, pval.

- format:

  Logical. Whether to format input files into LDSC format.

- python_path:

  Character. Path to Python in the LDSC conda env.

- munge_script:

  Character. Path to munge_sumstats.py.

- merge_alleles:

  Character. Path to w_hm3.snplist.

- chunksize:

  Integer. munge_sumstats chunksize.

- run_rg:

  Logical. Whether to run ldsc.py –rg.

- rg_ref:

  Character. Reference sumstats.gz file for rg (e.g., MASLD).

- ldsc_script:

  Character. Path to ldsc.py.

- ref_ld_chr:

  Character. Path to ref-ld-chr directory.

- w_ld_chr:

  Character. Path to w-ld-chr directory.

- rg_out_dir:

  Character. Output directory for rg results.

## Value

A list with formatted files, munged files, and rg outputs (if run).
