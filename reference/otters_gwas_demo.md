# Demo data for OTTERS GWAS formatting

Example GWAS summary tables for three supported schemas: "Mun",
"exposure", and "outcome".

## Usage

``` r
otters_gwas_demo
```

## Format

A list with three data.frames:

- mun:

  Columns: \`CHR\`, \`BP\`, \`A1\`, \`A2\`, \`BETA\`, \`P\`.

- exposure:

  Columns: \`chr.exposure\`, \`pos.exposure\`,
  \`effect_allele.exposure\`, \`other_allele.exposure\`,
  \`beta.exposure\`, \`pval.exposure\`.

- outcome:

  Columns: \`chr.outcome\`, \`pos.outcome\`, \`effect_allele.outcome\`,
  \`other_allele.outcome\`, \`beta.outcome\`, \`pval.outcome\`.

## Source

Simulated example for documentation and testing.
