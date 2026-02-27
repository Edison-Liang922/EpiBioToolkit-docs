# SHAP summary plot (Python shap)

Draw a SHAP summary plot using the Python `shap` package via reticulate.

## Usage

``` r
plot_shap_summary(
  shap_values,
  X,
  save_path = NULL,
  width = 12,
  height = 8,
  dpi = 300
)
```

## Arguments

- shap_values:

  SHAP values (2D array or matrix).

- X:

  Feature matrix/data.frame used for SHAP plotting.

- save_path:

  Optional. File path to save the plot (PDF/PNG).

- width:

  Plot width in inches (passed to matplotlib).

- height:

  Plot height in inches (passed to matplotlib).

- dpi:

  Plot DPI.

## Value

Invisibly returns a list with `shap` and `plt` handles.

## Required inputs

- shap_values:

  2D SHAP values (samples x features).

- X:

  Feature matrix/data.frame with matching columns.
