# Gather graph edges from a data.frame

Create edge table for circular hierarchical graphs.

## Usage

``` r
gather_graph_edge(df, index = NULL, root = NULL)
```

## Arguments

- df:

  A data.frame.

- index:

  Character vector of grouping columns (at least two).

- root:

  Character. Optional root node name.

## Value

A tibble with edge attributes.
