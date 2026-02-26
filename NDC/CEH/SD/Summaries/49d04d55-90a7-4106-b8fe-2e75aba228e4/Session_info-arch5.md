R VERSION 3.5.3 TESTING INFORMATION
- Purpose and context: Information about testing the application and analysis routines using R version 3.5.3.
- Platform and execution environment:
  - Operating system: Windows 10 x64 (build 14393)
  - CPU/architecture: x86_64-w64-mingw32/x64 (64-bit)
  - Matrix products: default
- Locale settings:
  - LC_COLLATE=English_United Kingdom.1252
  - LC_CTYPE=English_United Kingdom.1252
  - LC_MONETARY=English_United Kingdom.1252
  - LC_NUMERIC=C
  - LC_TIME=English_United Kingdom.1252
- Base and attached packages:
  - Base: grid, stats, graphics, grDevices, utils, datasets, methods, base
  - Attached: openxlsx_4.2.2, sets_1.0-18, dplyr_0.8.0.1, changepoint_2.3.1, zoo_1.8-6, lubridate_1.7.4, tseries_0.10-46, ggplot2_3.1.0, shinycssloaders_0.3, shinyjs_1.0, shiny_1.2.0
- Namespace-loaded dependencies (selected highlights):
  - zip_2.0.4, Rcpp_1.0.0, pillar_1.3.1, compiler_3.5.3, later_0.8.0, plyr_1.8.4, xts_0.11-2, tools_3.5.3, digest_0.6.18, jsonlite_1.6, lattice_0.20-38, tibble_2.0.1, gtable_0.2.0, pkgconfig_2.0.2, rlang_0.3.1, crosstalk_1.0.0, curl_3.3, yaml_2.2.0, stringr_1.4.0, withr_2.1.2, htmlwidgets_1.3, DT_0.5, tidyselect_0.2.5, glue_1.3.0, R6_2.4.0, TTR_0.23-4, purrr_0.3.0, magrittr_1.5, scales_1.0.0, promises_1.0.1, htmltools_0.3.6, quantmod_0.4-13, assertthat_0.2.0, mime_0.6, xtable_1.8-3, colorspace_1.4-0, httpuv_1.4.5.1, labeling_0.3, quadprog_1.5-5, stringi_1.3.1, lazyeval_0.2.1, munsell_0.5.0, crayon_1.3.4
- Observations for governance relevance:
  - Provides a clear audit trail of the exact software environment used for testing, supporting reproducibility and dataset governance across systems.
  - Highlights dependency breadth (data manipulation, visualization, interactivity, time-series, and governance-relevant packages) that could influence data processing and metadata capture.

R VERSION 3.6.1 TESTING INFORMATION
- Purpose and context: Information about testing the application and analysis routines using R version 3.6.1.
- Platform and execution environment:
  - Operating system: Windows 10 x64 (build 14393)
  - CPU/architecture: x86_64-w64-mingw32/x64 (64-bit)
  - Matrix products: default
- Locale settings:
  - LC_COLLATE=English_United Kingdom.1252
  - LC_CTYPE=English_United Kingdom.1252
  - LC_MONETARY=English_United Kingdom.1252
  - LC_NUMERIC=C
  - LC_TIME=English_United Kingdom.1252
- Base and attached packages:
  - Base: grid, stats, graphics, grDevices, utils, datasets, methods, base
  - Attached: openxlsx_4.1.4, sets_1.0-18, dplyr_0.8.0.1, changepoint_2.2.2, zoo_1.8-8, lubridate_1.7.4, tseries_0.10-46, ggplot2_3.3.2, shinycssloaders_1.0.0, shinyjs_2.0.0, shiny_1.5.0
- Namespace-loaded dependencies (selected highlights):
  - zip_2.1.1, Rcpp_1.0.5, pillar_1.4.7, compiler_3.6.1, later_1.1.0.1, xts_0.12.1, tools_3.6.1, digest_0.6.27, jsonlite_1.7.1, lattice_0.20-41, lifecycle_0.2.0, tibble_3.0.4, gtable_0.3.0, pkgconfig_2.0.3, rlang_0.4.8, crosstalk_1.1.1, curl_4.3, yaml_2.2.1, fastmap_1.0.1, stringr_1.4.0, withr_2.3.0, vctrs_0.3.5, htmlwidgets_1.5.2, DT_0.17, tidyselect_1.1.0, glue_1.4.2, R6_2.5.0, farver_2.0.3, TTR_0.24.2, purrr_0.3.4, magrittr_2.0.1, scales_1.1.1, promises_1.1.1, ellipsis_0.3.1, htmltools_0.5.0, quantmod_0.4.17, assertthat_0.2.1, mime_0.9, xtable_1.8-4, colorspace_2.0-0, httpuv_1.5.4, labeling_0.4.2, quadprog_1.5-8, stringi_1.5.3, munsell_0.5.0, crayon_1.3.4
- Observations for governance relevance:
  - Demonstrates testing across a newer R version with updated packages, indicating ongoing maintenance and compatibility checks across environments.
  - Shows changes in key packages (e.g., openxlsx, changepoint, ggplot2, shinyjs, shinycssloaders) that can affect data handling, visualization, and interactive reporting.
  - Retains locale and platform details to support reproducible data processing and metadata for datasets and analyses.

Overall governance notes for Data Stewards
- The document provides explicit environment snapshots (R version, OS, locale) that are essential for reproducibility, consistent data processing, and audit trails when datasets and analyses are shared or re-used.
- The inclusion of major and namespace package lists highlights the dependencies that influence data workflows, formatting, and reporting. This is important for documenting standards, versioning, and any potential compatibility issues across datasets or systems.
- Notable version differences between the two environments should be tracked in metadata when sharing analyses or datasets, to ensure users can reproduce results under equivalent conditions.