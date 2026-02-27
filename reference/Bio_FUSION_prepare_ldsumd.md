# Prepare FUSION LDSUMD Files

Split GWAS summary statistics into per-chromosome \`.ldsumd\` files for
FUSION.

## Usage

``` r
Bio_FUSION_prepare_ldsumd(
  gwas_files,
  output_dir = NULL,
  chr_col = "chr",
  snp_col = "SNP",
  a1_col = "A1",
  a2_col = "A2",
  z_col = "Z",
  drop_empty_snp = TRUE,
  sep = " ",
  quote = FALSE
)
```

## Arguments

- gwas_files:

  Character vector of GWAS file paths.

- output_dir:

  Output directory. If \`NULL\`, use each input file's directory.

- chr_col:

  Column name for chromosome.

- snp_col:

  Column name for SNP ID.

- a1_col:

  Column name for effect allele.

- a2_col:

  Column name for other allele.

- z_col:

  Column name for Z-score.

- drop_empty_snp:

  Logical; drop empty/NA SNP IDs.

- sep:

  Separator for output files (default \`" "\`).

- quote:

  Logical; whether to quote output fields.

## Value

A named list of output file paths by GWAS prefix.
