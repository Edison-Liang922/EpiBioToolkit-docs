# LDSC analysis with the ldscr R package

Prepare sumstats for ldscr and run heritability (h2) and genetic
correlation (rg) analyses.

## Usage

``` r
Bio_LDSC_R(
  sumstats_list,
  traits = NULL,
  col_map = list(snp = "SNP", a1 = "A1", a2 = "A2", beta = "BETA", se = "SE", n = "N"),
  ancestry = "EUR",
  run_h2 = TRUE,
  run_rg = TRUE
)
```

## Arguments

- sumstats_list:

  List of data.frames. Each data.frame must contain columns for SNP, A1,
  A2, BETA, SE, and N (see `col_map`).

- traits:

  Character vector. Trait names (same length as sumstats_list).

- col_map:

  Named list mapping standard names to input columns: snp, a1, a2, beta,
  se, n.

- ancestry:

  Character. Ancestry label passed to ldscr.

- run_h2:

  Logical. Whether to run `ldsc_h2` for each trait.

- run_rg:

  Logical. Whether to run `ldsc_rg` for all traits.

## Value

A list with:

- \`munged_list\`: list of formatted data.frames (SNP, N, Z, A1, A2).

- \`h2\`: combined h2 results (if run_h2).

- \`rg\`: rg results table (if run_rg).
