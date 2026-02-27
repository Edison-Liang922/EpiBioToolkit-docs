# GSEA Pipeline for Bulk RNA-seq

Run GSEA from differential expression results and save outputs.

## Usage

``` r
Bio_Bulk_gsea_pipeline(
  deg_results,
  gmt_file = NULL,
  project_name = "Project",
  org_db = "org.Hs.eg.db",
  organism = "hsa",
  pvalue_cutoff = 0.05
)
```

## Arguments

- deg_results:

  Differential expression results with \`gene\` (gene symbol) and
  \`logFC\` (log2 fold-change).

- gmt_file:

  Optional GMT file path (e.g., MSigDB C7). If \`NULL\`, run KEGG GSEA.

- project_name:

  Project name for output files.

- org_db:

  Organism annotation package name or OrgDb object (default:
  "org.Hs.eg.db").

- organism:

  KEGG organism code (default: "hsa").

- pvalue_cutoff:

  P-value cutoff for GSEA (used for plotting/filtering).

## Value

A \`gseaResult\` object.
