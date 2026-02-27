# Demo data for OTTERS eQTL formatting

A small example list containing:

- \`eqtl\`: formatted eQTL summary table (as produced by
  `Bio_OTTERS_format_eqtl`)

- \`anno\`: gene annotation table for OTTERS

## Usage

``` r
otters_eqtl_demo
```

## Format

A list with two data.frames:

- eqtl:

  Data frame with columns: \`CHROM\`, \`POS\`, \`A1\`, \`A2\`,
  \`Zscore\`, \`TargetID\`, \`N\`.

- anno:

  Data frame with columns: \`CHROM\`, \`GeneStart\`, \`GeneEnd\`,
  \`TargetID\`.

## Source

Simulated example for documentation and testing.
