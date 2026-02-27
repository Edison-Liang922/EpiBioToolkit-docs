# Run FUSION Commands in Parallel

Execute a vector of system commands with optional parallelization.

## Usage

``` r
Bio_FUSION_run_cmds(cmds, workers = 4, use_mclapply = TRUE)
```

## Arguments

- cmds:

  Character vector of command strings.

- workers:

  Number of parallel workers.

- use_mclapply:

  Use \`parallel::mclapply\` (Linux/macOS) when TRUE; otherwise use
  \`lapply\`.

## Value

A list of command outputs (character vectors).
