# Format GWAS summary for OTTERS

Convert GWAS summary statistics into OTTERS-required format with
columns: \`CHROM\`, \`POS\`, \`A1\`, \`A2\`, \`Zscore\`. Supports three
input schemas:

- `source = "Mun"`: columns `CHR, BP, A1, A2, BETA, P`

- `source = "exposure"`: columns
  `chr.exposure, pos.exposure, effect_allele.exposure, other_allele.exposure, beta.exposure, pval.exposure`

- `source = "outcome"`: columns
  `chr.outcome, pos.outcome, effect_allele.outcome, other_allele.outcome, beta.outcome, pval.outcome`

## Usage

``` r
Bio_OTTERS_format_gwas(dat, save_name, source = "Mun", one_chr_allele = TRUE)
```

## Arguments

- dat:

  A data.frame containing GWAS summary statistics.

- save_name:

  Character scalar. Output file path for the formatted table.

- source:

  Character. One of `"Mun"`, `"exposure"`, `"outcome"`.

- one_chr_allele:

  Logical. Whether to keep only SNPs with single-base alleles. Default
  TRUE.

## Value

A data.frame with columns: `CHROM, POS, A1, A2, Zscore`.

## Details

Z scores are computed as \`sign(BETA) \* abs(qnorm(P/2))\`. For \`source
= "Mun"\`, A1/A2 are swapped to keep the same orientation as the
original script. When \`one_chr_allele = TRUE\`, variants with
multi-base alleles are removed. The formatted table is written to
\`save_name\` as a tab-delimited file.

## See also

\[Bio_OTTERS_format_eqtl()\]
