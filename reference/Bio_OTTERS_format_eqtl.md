# Format eQTL summary for OTTERS stage 1

Prepare OTTERS training inputs from SMR eQTL files. This function is
intended for OTTERS stage 1 (training) and produces:

- main summary file: \*\_hg38.txt

- gene mapping file: \*\_gene_mapping.txt

- annotation file: \*\_hg38_anno.txt

## Usage

``` r
Bio_OTTERS_format_eqtl(
  exe,
  beqtl,
  out_path,
  N,
  hg19to38 = TRUE,
  thread = 8,
  smr_fun = NULL,
  liftover_fun = NULL
)
```

## Arguments

- exe:

  保留参数，暂不使用。

- beqtl:

  Character scalar. Path to the SMR eQTL summary file (e.g., .besd). A
  sidecar file \`beqtl.epi\` must exist.

- out_path:

  Character scalar. Output directory for generated files.

- N:

  Numeric scalar. Sample size.

- hg19to38:

  Logical. Whether to lift from GRCh37 to GRCh38. Default TRUE.

- thread:

  Integer. Threads used by \`smr_summary_xqtl\`.

- smr_fun:

  Optional function. If provided, used instead of \`smr_summary_xqtl\`
  to extract eQTL summary. It must accept the same arguments and return
  a data.frame with columns: \`SNP\`, \`Chr\`, \`BP\`, \`A1\`, \`A2\`,
  \`b\`, \`p\`, \`Probe\`.

- liftover_fun:

  Optional function used when \`hg19to38 = TRUE\`. It must accept a
  data.frame plus \`convert_ref_genome\` and \`ref_genome\` arguments
  and return a data.frame with lifted coordinates.

## Value

A list with elements:

- \`eqtl\`: formatted summary table with columns \`CHROM\`, \`POS\`,
  \`A1\`, \`A2\`, \`Zscore\`, \`TargetID\`, \`N\`

- \`mapping\`: gene mapping table (\`CHROM\`, \`GeneStart\`,
  \`GeneEnd\`, \`TargetID\`)

- \`anno\`: annotation table (\`CHROM\`, \`GeneStart\`, \`GeneEnd\`,
  \`TargetID\`)

- \`files\`: list of output file paths

## Details

Required inputs:

- \`beqtl\` is an SMR eQTL summary file. A sidecar \`beqtl.epi\` file
  must exist. The \`.epi\` file should include at least 4 columns where
  V1 = chromosome, V2 = probe or target ID, and V4 = probe position.

Z scores are computed as \`sign(BETA) \* abs(qnorm(P/2))\`. If
\`hg19to38 = TRUE\`, coordinates are lifted from GRCh37 to GRCh38 using
\`liftover\` (or a provided \`liftover_fun\`). Output tables are written
to \`out_path\` and sorted by CHROM and POS.

## See also

\[Bio_OTTERS_format_gwas()\], \[Bio_OTTERS_create_sh_stage1()\]
