# Circulating Branch-Chain Amino Acids and Blood Pressure: A Mendelian Randomization Study

<!-- badges: start -->
<!-- badges: end -->

This repository contains R code to reproduce Mendelian randomization analyses evaluating the relationship between branch-chain amino acids and blood pressure. The results of these analyses are published as part of:

*Murashige et. al. (2022). Extra-cardiac BCAA catabolism lowers blood pressure and protects from heart failure.*

## Usage
The following steps should allow the user to reproduce the `BCAA-BP-MR.html` document, which contains additional description of the data sources, methods, and rendered plots/tables/results:

1. Clone/download the contents of this repository into a new directory.
1. Open `BCAA-BP-MR.qmd` in [RStudio](https://www.rstudio.com/) and/or render the document using [Quarto](https://quarto.org/). This file is a Quarto markdown document, including code and text which when rendered reproduce the `BCAA-BP-MR.html` document.

## Notes
- All required R package dependencies have been captured by the `renv` package (https://rstudio.github.io/renv/index.html), and are stored in `renv.lock`. All required packages will be automatically installed using the `renv::restore()` function when the document is rendered.
- Summary genetic data used to construct genetic instruments for branch chain amino acids and the corresponding effects on blood pressure traits will be queried from the [IEU OpenGWAS Project](https://gwas.mrcieu.ac.uk/), or downloaded from the [Pan-UK Biobank project](https://pan.ukbb.broadinstitute.org/) into the `Data/` directory. These files are large (~2GB each), and are therefore not included in the repository directly.
- The `Data/` directory contains additional information needed to test for enrichment of BCAA-associated genetic variants with genes known to be involved in BCAA metabolism (additional details described in `BCAA-BP-MR.qmd`).
- Where possible the document reads from cached results located in the `BCAA-BP-MR_cache/` and `BCAA-BP-MR_files/` directories to speed up rendering. To render the document entirely from scratch, change `cache: true` to `cache: false` in the YAML header of `BCAA-BP-MR.qmd`.

## System Requirements
- RAM: 32GB (recommended when rendering from scratch, as GWAS summary statistics from Pan-UK Biobank are large; memory requirement should be lower when rendering from cached output or excluding Pan UK Biobank analyses)


