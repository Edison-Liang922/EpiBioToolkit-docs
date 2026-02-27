# Virtual knockout analysis with scTenifoldKnk

Run scTenifoldKnk using a Seurat object or a raw count matrix.

## Usage

``` r
Bio_scRNA_scTenifoldKnk(
  object = NULL,
  countMatrix = NULL,
  assay = NULL,
  layer = "counts",
  slot = "counts",
  gKO,
  qc = TRUE,
  qc_mtThreshold = 0.1,
  qc_minLSize = 1000,
  nCores = parallel::detectCores(),
  ...
)
```

## Arguments

- object:

  A Seurat object (optional). If provided, \`countMatrix\` is extracted
  via GetAssayData.

- countMatrix:

  A raw count matrix (genes x cells). If provided, \`object\` is
  ignored.

- assay:

  Assay name used when extracting from Seurat (default: DefaultAssay).

- layer:

  Layer name for Seurat v5 (default "counts").

- slot:

  Slot name for Seurat v4 (default "counts").

- gKO:

  Character. Gene symbol to knock out.

- qc:

  Logical. Apply QC inside scTenifoldKnk.

- qc_mtThreshold:

  Max mitochondrial proportion for QC.

- qc_minLSize:

  Minimum library size for QC.

- nCores:

  Number of cores (default parallel::detectCores()).

- ...:

  Additional arguments passed to scTenifoldKnk.

## Value

The scTenifoldKnk result object.
