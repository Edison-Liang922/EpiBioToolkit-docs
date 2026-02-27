# GO/KEGG ORA Enrichment Analysis

Run GO and KEGG over-representation analysis from DEG results.

## Usage

``` r
Bio_Bulk_ora_enrichment(
  deg_results,
  project_name = "Project",
  org_db = "org.Hs.eg.db",
  pvalue_cutoff = 0.05
)
```

## Arguments

- deg_results:

  Differential expression results with \`gene\` (gene symbol) and
  \`change\` (up/down/stable).

- project_name:

  Project name for output files.

- org_db:

  Organism annotation package name or OrgDb object (default:
  "org.Hs.eg.db").

- pvalue_cutoff:

  P-value cutoff for enrichment.

## Value

A list with GO and KEGG enrichment tables.
