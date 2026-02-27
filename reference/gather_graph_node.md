# Gather graph nodes from a data.frame

Create node table for circular hierarchical graphs.

## Usage

``` r
gather_graph_node(df, index = NULL, value = tail(colnames(df), 1), root = NULL)
```

## Arguments

- df:

  A data.frame.

- index:

  Character vector of grouping columns (at least two).

- value:

  Character. Column name used as node size. Default is the last column.

- root:

  Character. Optional root node name.

## Value

A tibble with node attributes.
