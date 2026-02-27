# Align Bulk Expression and Group Metadata

Rename sample IDs, recode group labels, and align expression rows with
group metadata.

## Usage

``` r
Bio_Bulk_align_group(
  expr,
  group,
  sample_col = "GSM",
  group_col = "group",
  dataset_col = "Dataset",
  id_prefix = "Data",
  recode_map = c(normal = "Control", cirrhosis = "Case"),
  keep_group_cols = NULL,
  reorder = TRUE
)
```

## Arguments

- expr:

  Expression matrix/data frame with sample IDs in row names.

- group:

  Sample metadata data frame. Must contain sample IDs (\`sample_col\`)
  and group labels (\`group_col\`).

- sample_col:

  Column name in \`group\` containing sample IDs.

- group_col:

  Column name in \`group\` containing group labels.

- dataset_col:

  Column name to use for the renamed sample IDs.

- id_prefix:

  Prefix for new sample IDs (e.g., "Data").

- recode_map:

  Named character vector for recoding group labels.

- keep_group_cols:

  Optional character vector of columns to keep in \`group\`.

- reorder:

  Logical; whether to reorder and subset to common samples.

## Value

A list with:

- expr:

  Expression data with renamed row names.

- group:

  Group data with renamed sample IDs and recoded labels.

- id_map:

  Named vector mapping original IDs to new IDs.
