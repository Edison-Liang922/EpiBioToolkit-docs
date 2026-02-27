# Demo eQTL Colocalization Data

A small demo eQTL dataset derived from the original \`eQTL_Coloc.txt\`
input. This dataset is intended for examples and testing.

## Usage

``` r
eqtl_coloc_demo
```

## Format

A data frame with 1500 rows and the following columns:

- SNP:

  Variant ID.

- Chr:

  Chromosome for the variant.

- BP:

  Base-pair position for the variant.

- A1:

  Effect allele.

- A2:

  Other allele.

- Freq:

  Effect allele frequency.

- Probe:

  Probe ID.

- Probe_Chr:

  Chromosome for the probe.

- Probe_bp:

  Base-pair position for the probe.

- Gene:

  Gene symbol.

- Orientation:

  Probe orientation.

- b:

  Effect size.

- SE:

  Standard error.

- p:

  P-value.

- n:

  Sample size.

## Source

Derived from \`eQTL_Coloc.txt\`.
