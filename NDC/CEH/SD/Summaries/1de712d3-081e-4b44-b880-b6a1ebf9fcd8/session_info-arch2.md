# sessionInfo()

## Purpose

- Capture the exact R session state to support reproducibility, audit trails, and consistent analysis of environmental monitoring data over time.

## Environment Details

- R version: 3.5.3 (2019-03-11)
- Platform: x86_64-pc-linux-gnu (64-bit)
- Operating System: Debian GNU/Linux 9 (stretch)
- BLAS/LAPACK: OpenBLAS base
- Locale: en_US.UTF-8 for most categories (CTYPE, TIME, COLLATE, MONETARY, PAPER, IDENTIFICATION); numeric locale set to C

## Software Stack

- Attached base packages: stats, graphics, grDevices, utils, datasets, methods, base
- Attached non-base packages (core for data manipulation, visualization, and web apps): DT, shinycssloaders, plotly, forcats, stringr, dplyr, purrr, readr, tidyr, tibble, ggplot2, tidyverse, shiny
- This combination indicates standardised workflows for data cleaning, transformation, visualization, and interactive reporting/dashboards

## Namespace-Loaded Packages

- A broad set of additional packages loaded via namespaces, enabling advanced data handling, visualization, spatial/temporal processing, reporting, and web app capabilities (examples include haven, lattice, colorspace, htmltools, viridisLite, yaml, rlang, glue, modelr, readxl, data.table, rvest, htmlwidgets, crosstalk, httpuv, broom, Rcpp, jsonlite, lubridate, httr, rstudioapi, nlme, compiler, among others)

## Implications for Environmental Monitoring

- The session snapshot supports consistent, auditable analyses of environmental health data by documenting the exact software environment and versions used.
- The combination of data-wrangling (e.g., dplyr, tidyr), visualization (ggplot2, plotly), and interactive reporting (shiny, DT) aligns with typical monitoring workflows that produce reports, maps, and dashboards.
- Clear reproducibility enables others to verify outputs, reuse datasets, and upload or share results through standard portals or dashboards, addressing the archetype’s emphasis on accessible underlying data and standardized outputs.