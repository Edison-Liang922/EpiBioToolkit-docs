# SMR helpers

Utility wrappers for SMR workflows: locating binaries, preparing input
files, running SMR, and summarizing xQTL results.

## Usage

``` r
Bio_SMR_local()

Bio_SMR_path(path)

Bio_SMR_check_snp(dat, ea_col, nea_col, source = NULL)

Bio_SMR_create_BESD(
  dat,
  gene_anno,
  SNP_col,
  ea_col,
  nea_col,
  beta_col,
  se_col,
  pval_col,
  chr_col,
  pos_col,
  freq_col,
  probe_col,
  gene_col,
  probe_col_anno,
  gene_col_anno,
  chr_col_anno,
  pos_col_anno,
  source = NULL,
  out_name,
  cl = NULL,
  split_snp = FALSE,
  split_sep = ",",
  check_allele = FALSE
)

Bio_SMR_create_ma(
  file = NULL,
  dat = NULL,
  out_file,
  source = NULL,
  overlap_split = TRUE,
  overlap_sep = ",",
  trans_na = TRUE,
  return = TRUE,
  only_rsid = TRUE
)

Bio_SMR_extract2BESD(
  beqtl = NULL,
  out,
  gene = NULL,
  extract_snp = NULL,
  extract_probe = NULL,
  qfile = NULL,
  pval = 5e-08,
  cluster = 10
)

Bio_SMR_run(
  gwas_summary,
  bfile,
  beqtl,
  out_path,
  gene = NULL,
  probe = NULL,
  wind = 5000,
  out_name = NULL,
  cl = NULL,
  return_code = FALSE,
  run = "smr"
)

Bio_SMR_summary_xqtl(
  snp = NULL,
  beqtl,
  out_path,
  query = 5e-08,
  out_name = NULL,
  gene = NULL,
  probe = NULL,
  type = "normal",
  wind = 2000,
  thread = 1
)
```
