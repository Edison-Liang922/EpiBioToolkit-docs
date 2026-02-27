# Demo data for SMR

Example input tables for SMR helper functions.

## Usage

``` r
smr_demo
```

## Format

A list with:

- eqtl:

  eQTL table with columns `SNP`, `CHR`, `BP`, `A1`, `A2`, `Freq`,
  `Beta`, `SE`, `P`, `Probe`, `Gene`.

- gene_anno:

  Annotation table with columns `Chr`, `ProbeID`, `ProbeBp`, `Gene`.

- gwas_ma:

  GWAS .ma-style table with columns `SNP`, `A1`, `A2`, `freq`, `b`,
  `se`, `p`.

## Source

Simulated example for documentation and testing.
