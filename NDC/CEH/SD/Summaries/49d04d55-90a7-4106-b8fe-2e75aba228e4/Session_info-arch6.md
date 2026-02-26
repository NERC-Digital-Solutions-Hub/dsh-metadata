# ----------R VERSION 3.5.3 TESTING INFORMATION----------

- Purpose
  - Documents testing environments for an application and related analysis routines across R versions, focusing on platform, locale, and package ecosystems used to validate functionality.

## R VERSION 3.5.3 TESTING INFORMATION

- Environment
  - R version: 3.5.3 (2019-03-11)
  - Platform: x86_64-w64-mingw32/x64 (64-bit)
  - OS: Windows 10 x64 (build 14393)
  - Locale: English (United Kingdom) for collate, ctype, monetary, and time; numeric locale is C

- Attached base packages
  - grid, stats, graphics, grDevices, utils, datasets, methods, base

- Other attached packages
  - openxlsx_4.2.2, sets_1.0-18, dplyr_0.8.0.1
  - changepoint_2.3.1, zoo_1.8-6, lubridate_1.7.4
  - tseries_0.10-46, ggplot2_3.1.0, shinycssloaders_0.3
  - shinyjs_1.0, shiny_1.2.0

- Loaded via namespace (selected highlights)
  - zip_2.0.4, Rcpp_1.0.0, pillar_1.3.1, compiler_3.5.3
  - later_0.8.0, plyr_1.8.4, xts_0.11-2, tools_3.5.3
  - digest_0.6.18, jsonlite_1.6, lattice_0.20-38, tibble_2.0.1
  - gtable_0.2.0, pkgconfig_2.0.2, rlang_0.3.1, crosstalk_1.0.0
  - curl_3.3, yaml_2.2.0, stringr_1.4.0, withr_2.1.2
  - htmlwidgets_1.3, DT_0.5, tidyselect_0.2.5, glue_1.3.0
  - R6_2.4.0, TTR_0.23-4, purrr_0.3.0, magrittr_1.5
  - scales_1.0.0, promises_1.0.1, htmltools_0.3.6, quantmod_0.4-13
  - assertthat_0.2.0, mime_0.6, xtable_1.8-3, colorspace_1.4-0
  - httpuv_1.4.5.1, labeling_0.3, quadprog_1.5-5, stringi_1.3.1
  - lazyeval_0.2.1, munsell_0.5.0, crayon_1.3.4

- Key takeaways for Data Support use
  - Demonstrates a robust testing setup across a major R version with emphasis on data handling, transformation, and visualization tools (e.g., dplyr, lubridate, ggplot2, DT, htmlwidgets).
  - Supports data product development with Shiny (shiny, shinyjs, shinycssloaders) and Excel I/O (openxlsx).
  - Indicates dependency breadth via numerous namespaces, underscoring the need for careful dependency management when deploying data dashboards and self-serve tools.

---

## R VERSION 3.6.1 TESTING INFORMATION

- Environment
  - R version: 3.6.1 (2019-07-05)
  - Platform: x86_64-w64-mingw32/x64 (64-bit)
  - OS: Windows 10 x64 (build 14393)
  - Locale: English (United Kingdom) for collate, ctype, monetary, and time; numeric locale is C

- Attached base packages
  - grid, stats, graphics, grDevices, utils, datasets, methods, base

- Other attached packages
  - openxlsx_4.1.4, sets_1.0-18, dplyr_0.8.0.1
  - changepoint_2.2.2, zoo_1.8-8, lubridate_1.7.4
  - tseries_0.10-46, ggplot2_3.3.2, shinycssloaders_1.0.0
  - shinyjs_2.0.0, shiny_1.5.0

- Loaded via namespace (selected highlights)
  - zip_2.1.1, Rcpp_1.0.5, pillar_1.4.7, compiler_3.6.1
  - later_1.1.0.1, xts_0.12.1, tools_3.6.1, digest_0.6.27
  - jsonlite_1.7.1, lattice_0.20-41, lifecycle_0.2.0, tibble_3.0.4
  - gtable_0.3.0, pkgconfig_2.0.3, rlang_0.4.8, crosstalk_1.1.1
  - curl_4.3, yaml_2.2.1, fastmap_1.0.1, stringr_1.4.0
  - withr_2.3.0, vctrs_0.3.5, htmlwidgets_1.5.2, DT_0.17
  - tidyselect_1.1.0, glue_1.4.2, R6_2.5.0, farver_2.0.3
  - TTR_0.24.2, purrr_0.3.4, magrittr_2.0.1, scales_1.1.1
  - promises_1.1.1, ellipsis_0.3.1, htmltools_0.5.0, quantmod_0.4.17
  - assertthat_0.2.1, mime_0.9, xtable_1.8-4, colorspace_2.0-0
  - httpuv_1.5.4, labeling_0.4.2, quadprog_1.5-8, stringi_1.5.3
  - munsell_0.5.0, crayon_1.3.4

- Key takeaways for Data Support use
  - Confirms continued compatibility testing in a newer R release with an updated set of visualization, I/O, and data manipulation packages.
  - Maintains emphasis on self-serve data tools via Shiny and interactive outputs (DT, htmlwidgets), with updated dependencies to reflect current ecosystem best practices.
  - Highlights the importance of tracking package versions across R upgrades to ensure reliable data products for end users.