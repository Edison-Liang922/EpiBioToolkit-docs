# Demo data for gene correlation plots

Example input for `plot_gene_pair_cor` and `plot_gene_deg_cor_parallel`.

## Usage

``` r
gene_cor_demo
```

## Format

A list with:

- expr:

  Expression matrix (genes x samples).

- deg_table:

  Data frame with columns `gene` and `change`.

- target_gene:

  Target gene for DEG correlation.

- gene1:

  First gene for pair correlation.

- gene2:

  Second gene for pair correlation.

## Source

Simulated example for documentation and testing.
