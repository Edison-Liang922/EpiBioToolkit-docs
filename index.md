# EpiBioToolkit (EBT)

*Epidemiology & Bioinformatics eXplorer*

EpiBioToolkit (EBT) is an R toolkit for epidemiology and omics
workflows, with emphasis on reproducible analysis, well-documented
inputs, and publication-ready plots. It also includes a single-cell
module for QC, integration, clustering, annotation, and downstream
analyses.

## Installation

``` r

# Private GitHub install (requires token)
Sys.setenv(GITHUB_PAT = "YOUR_TOKEN")
remotes::install_github("Edison-Liang922/EpiBioToolkit")

# Local install (if you have the source)
devtools::install("/Users/edisonliang/Desktop/R包打包/EpiBioToolkit")
```

## Quick start

``` r

library(EpiBioToolkit)

# MR pipeline demo
data("mr_demo")
res <- Bio_MR_pipeline(
  exposure_data_list = mr_demo$exposure_list,
  exposure_names = mr_demo$exposure_names,
  outcome_data = mr_demo$outcome_data,
  out_dir = "mr_results"
)
```

## Scope

- Mendelian randomization (Bio_MR\_\*)
- Colocalization and INTACT
- Bulk RNA-seq (limma, WGCNA, enrichment)
- TWAS / FUSION utilities
- Single-cell workflows (QC, integration, clustering, annotation)
- Diagnostics (ML, ROC, calibration)
- Visualization (Manhattan, Venn, Love, etc.)

## Authors

- Weixuan Liang (aka Edison Liang)
- Ziyang Yang (aka Elder_sheep)
- Zhuofeng Wen (aka Tendy Wen)
- Jiahui Lai (aka Autumn_hill)

## Reference

- API index: `reference/index.html`
- Plot gallery: `reference/index.html#section-plots`
