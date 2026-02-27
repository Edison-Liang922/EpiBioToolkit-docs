# Create gsMAP batch shell script

Generate a bash script to run gsmap quick_mode followed by run_report
for combinations of HDF5 samples and GWAS sumstats.

## Usage

``` r
Bio_GSMAP_create_sh(
  hdf5_list,
  sumstats_list,
  workdir,
  gsmap_resource_dir,
  homolog_file,
  annotation = "H1_annotation",
  data_layer = "count",
  report_annotation = NULL,
  gsmap_cmd = "gsmap",
  log_dir = "/tmp",
  kill_pattern = "Step 5 completed",
  kill_signal = "-9",
  top_corr_genes = 2,
  point_size = 6,
  fig_width = 700,
  fig_height = 500,
  sample_name_fun = NULL,
  trait_name_fun = NULL,
  outfile = "gsmap_run.sh",
  make_executable = TRUE
)
```

## Arguments

- hdf5_list:

  Character vector of .h5ad paths.

- sumstats_list:

  Character vector of sumstats (.sumstats.gz) paths.

- workdir:

  Working directory for gsmap.

- gsmap_resource_dir:

  Path to gsMap_resource directory.

- homolog_file:

  Path to homologs file.

- annotation:

  Annotation name for quick_mode.

- data_layer:

  Data layer for quick_mode (e.g., "count").

- report_annotation:

  Annotation name for run_report. If NULL, use annotation.

- gsmap_cmd:

  gsmap executable or full path.

- log_dir:

  Directory for log files.

- kill_pattern:

  Pattern to detect completion in logs.

- kill_signal:

  Signal used to stop quick_mode (e.g., "-9").

- top_corr_genes:

  run_report: top_corr_genes.

- point_size:

  run_report: point_size.

- fig_width:

  run_report: fig_width.

- fig_height:

  run_report: fig_height.

- sample_name_fun:

  Function to derive sample name from hdf5 path. Default keeps the
  original rule: take basename and cut at the first underscore.

- trait_name_fun:

  Function to derive trait name from sumstats path. Default keeps the
  original rule: basename without `.sumstats.gz`.

- outfile:

  Output .sh file path.

- make_executable:

  Logical; chmod +x the output file.

## Value

The output script path (invisible).

## Details

Naming rules (same as your original shell):

- sample_name: `basename(HDF5_PATH)` then take the part before the first
  underscore (equivalent to `basename "$HDF5_PATH" | cut -d_ -f1`).

- trait_name: `basename(SUMSTATS_FILE)` with suffix `.sumstats.gz`
  removed.
