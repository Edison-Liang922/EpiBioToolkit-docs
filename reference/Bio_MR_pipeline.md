# Full MR pipeline

End-to-end MR workflow: process exposure -\> format outcome -\>
harmonise -\> MR analysis.

## Usage

``` r
Bio_MR_pipeline(
  exposure_data_list,
  exposure_names,
  outcome_data,
  exposure_col_map = list(snp = "SNP", beta = "BETA", se = "SE", eaf = "EAF",
    effect_allele = "A1", other_allele = "A2", pval = "P", n = "N", chr = "CHR", pos =
    "POS"),
  outcome_col_map = list(snp = "SNP", beta = "BETA", se = "SE", eaf = "EAF",
    effect_allele = "A1", other_allele = "A2", pval = "P", n = "N", chr = "CHR", pos =
    "POS"),
  outcome_name = "Outcome",
  filter_pval = 1e-05,
  filter_f = 10,
  clump_params = list(perform = TRUE, kb = 10000, r2 = 0.001, pval = 5e-08, local =
    FALSE, plink_bin = NULL, bfile = NULL),
  cores = 10,
  out_dir = "MR_results"
)
```

## Arguments

- exposure_data_list:

  List of raw exposure data.frames.

- exposure_names:

  Character vector of exposure names.

- outcome_data:

  data.frame. Raw outcome GWAS data.

- exposure_col_map:

  List. Column mapping for exposure data.

- outcome_col_map:

  List. Column mapping for outcome data.

- outcome_name:

  Character. Outcome phenotype name.

- filter_pval:

  Numeric. P-value threshold for exposure pre-filter.

- filter_f:

  Numeric. F-statistic threshold.

- clump_params:

  List. Parameters passed to `Bio_MR_process_exposure`.

- cores:

  Integer. Number of cores for harmonise and MR batch.

- out_dir:

  Character. Output directory for results.

## Value

A list with:

- \`exposure_list\`: processed exposure list.

- \`outcome_dat\`: formatted outcome data.

- \`harmonized_list\`: harmonised data list.

- \`completed\`: completed exposure names from MR batch.
