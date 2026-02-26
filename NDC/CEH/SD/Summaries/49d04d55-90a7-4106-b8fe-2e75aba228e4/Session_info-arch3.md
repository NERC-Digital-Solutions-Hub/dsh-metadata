# ----------R VERSION 3.5.3 TESTING INFORMATION----------

- Purpose of the document
  - Details the environments in which the application and its analysis routines were tested, focusing on R version compatibility and package dependencies.

- R version 3.5.3 testing
  - Platform: x86_64-w64-mingw32/x64 (64-bit) on Windows 10 x64 (build 14393)
  - Locale: English (United Kingdom) for collation, ctype, monetary; numeric and time settings as English UK; numeric set to C
  - Attached base packages: grid, stats, graphics, grDevices, utils, datasets, methods, base
  - Attached packages: openxlsx_4.2.2, sets_1.0-18, dplyr_0.8.0.1, changepoint_2.3.1, zoo_1.8-6, lubridate_1.7.4, tseries_0.10-46, ggplot2_3.1.0, shinycssloaders_0.3, shinyjs_1.0, shiny_1.2.0
  - Loaded via namespace (selected): zip_2.0.4, Rcpp_1.0.0, pillar_1.3.1, compiler_3.5.3, later_0.8.0, plyr_1.8.4, xts_0.11-2, tools_3.5.3, digest_0.6.18, jsonlite_1.6, lattice_0.20-38, tibble_2.0.1, gtable_0.2.0, pkgconfig_2.0.2, rlang_0.3.1, crosstalk_1.0.0, curl_3.3, yaml_2.2.0, stringr_1.4.0, withr_2.1.2, htmlwidgets_1.3, DT_0.5, tidyselect_0.2.5, glue_1.3.0, R6_2.4.0, TTR_0.23-4, purrr_0.3.0, magrittr_1.5, scales_1.0.0, promises_1.0.1, htmltools_0.3.6, quantmod_0.4-13, assertthat_0.2.0, mime_0.6, xtable_1.8-3, colorspace_1.4-0, httpuv_1.4.5.1, labeling_0.3, quadprog_1.5-5, stringi_1.3.1, lazyeval_0.2.1, munsell_0.5.0, crayon_1.3.4

- R version 3.6.1 testing
  - Platform: x86_64-w64-mingw32/x64 (64-bit) on Windows 10 x64 (build 14393)
  - Locale: English (United Kingdom) for collation, ctype, monetary; numeric and time settings as English UK
  - Attached base packages: grid, stats, graphics, grDevices, utils, datasets, methods, base
  - Attached packages: openxlsx_4.1.4, sets_1.0-18, dplyr_0.8.0.1, changepoint_2.2.2, zoo_1.8-8, lubridate_1.7.4, tseries_0.10-46, ggplot2_3.3.2, shinycssloaders_1.0.0, shinyjs_2.0.0, shiny_1.5.0
  - Loaded via namespace (selected): zip_2.1.1, Rcpp_1.0.5, pillar_1.4.7, compiler_3.6.1, later_1.1.0.1, xts_0.12.1, tools_3.6.1, digest_0.6.27, jsonlite_1.7.1, lattice_0.20-41, lifecycle_0.2.0, tibble_3.0.4, gtable_0.3.0, pkgconfig_2.0.3, rlang_0.4.8, crosstalk_1.1.1, curl_4.3, yaml_2.2.1, fastmap_1.0.1, stringr_1.4.0, withr_2.3.0, vctrs_0.3.5, htmlwidgets_1.5.2, DT_0.17, tidyselect_1.1.0, glue_1.4.2, R6_2.5.0, farver_2.0.3, TTR_0.24.2, purrr_0.3.4, magrittr_2.0.1, scales_1.1.1, promises_1.1.1, ellipsis_0.3.1, htmltools_0.5.0, quantmod_0.4.17, assertthat_0.2.1, mime_0.9, xtable_1.8-4, colorspace_2.0-0, httpuv_1.5.4, labeling_0.4.2, quadprog_1.5-8, stringi_1.5.3, munsell_0.5.0, crayon_1.3.4

- Observations relevant to monitoring framework authors
  - The document demonstrates cross-version testing (R 3.5.3 and 3.6.1) on a Windows platform, highlighting the importance of verifying compatibility and stability across R releases for monitoring tools.
  - It catalogs a substantial set of dependencies across time-series, data manipulation, visualization, and web interfaces (e.g., dplyr, zoo, tseries, changepoint, ggplot2, shiny, shinydisplay components), illustrating the complexity of environments that monitoring frameworks may encounter.
  - Metadata and provenance considerations are implicit through explicit listing of package versions and namespaces, underscoring the need for precise environment documentation to support reproducibility, audits, and governance.
  - The variation in package versions between the two R versions indicates that monitoring frameworks should account for evolving dependencies and ensure clear recording of software environments when evaluating environmental health measures.