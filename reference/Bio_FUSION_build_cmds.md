# Build FUSION Assoc Test Commands

Generate system commands for running FUSION association tests.

## Usage

``` r
Bio_FUSION_build_cmds(
  ldsumd_prefixes,
  weight_dirs,
  fusion_script,
  out_root,
  ld_ref_prefix,
  weight_pos_suffix = ".nofilter.pos",
  chr_vec = 1:22
)
```

## Arguments

- ldsumd_prefixes:

  Character vector of GWAS file prefixes (without .chr\*.ldsumd).

- weight_dirs:

  Character vector of weight directories (e.g., GTEx tissue folders).

- fusion_script:

  Path to FUSION.assoc_test.R.

- out_root:

  Output root directory for results.

- ld_ref_prefix:

  Path prefix to LD reference (e.g., ".../1000G.EUR.").

- weight_pos_suffix:

  Suffix for weight position file (e.g., ".nofilter.pos").

- chr_vec:

  Chromosome vector to run (default 1:22).

## Value

Character vector of command strings.
