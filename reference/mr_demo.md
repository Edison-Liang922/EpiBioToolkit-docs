# Demo data for MR workflow

Example exposure and outcome GWAS tables plus recommended parameters for
the MR pipeline.

## Usage

``` r
mr_demo
```

## Format

A list with the following fields:

- exposure_list:

  A list of two exposure data.frames. Each data.frame has columns:
  \`SNP\`, \`CHR\`, \`POS\`, \`A1\`, \`A2\`, \`EAF\`, \`BETA\`, \`SE\`,
  \`P\`, \`N\`.

- exposure_names:

  Character vector of exposure names.

- outcome_data:

  A data.frame with columns: \`SNP\`, \`CHR\`, \`POS\`, \`A1\`, \`A2\`,
  \`EAF\`, \`BETA\`, \`SE\`, \`P\`, \`N\`.

- exposure_col_map:

  Column mapping for exposure data.

- outcome_col_map:

  Column mapping for outcome data.

- clump_params:

  Clumping parameters (default demo uses `perform = FALSE`).

## Source

Simulated example for documentation and testing.
