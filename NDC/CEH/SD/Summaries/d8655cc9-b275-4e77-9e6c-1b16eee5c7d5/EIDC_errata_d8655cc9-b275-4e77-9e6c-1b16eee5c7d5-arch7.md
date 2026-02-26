# Errata for dataset http://doi.org/10.5285/d8655cc9-b275-4e779e6c-1b16eee5c7d5

- Issue
  - An error was found in the Met Office gridded monthly rainfall data for 1960–2000.
  - The Met Office cannot provide a corrected version in time because the dataset will be superseded by UKCP18 in March next year.

- CEH's corrective actions
  - Derived monthly rainfall grids for the problematic period from Met Office daily rainfall grids.
  - Recalculated the Standardized Precipitation Index (SPI) for the entire period using the corrected dataset.
  - Added an extra 9-month accumulation period based on feedback related to the superseded dataset.

- Implications for GIS workflows
  - Updated rainfall grids and SPI values may change historical analyses and map renderings for 1960–2000.
  - The introduction of a 9-month accumulation period affects time-series drought/rainfall visualizations and analyses.
  - The fix is CEH-generated and should be considered in provenance and reproducibility; users may need to re-run analyses with the corrected data.

- Data status and future considerations
  - This erratum serves as a temporary correction pending the UKCP18 data release next year.
  - Plan to transition to the UKCP18 dataset when available for long-term analyses.
  - Metadata should reflect the correction, the 9-month accumulation, and the affected period (1960–2000).

- Practical notes
  - The correction affects the dataset associated with the original DOI; verify whether updated versions or additional errata exist.
  - For policy or client-facing maps, communicate the changes to users and update visualizations accordingly.