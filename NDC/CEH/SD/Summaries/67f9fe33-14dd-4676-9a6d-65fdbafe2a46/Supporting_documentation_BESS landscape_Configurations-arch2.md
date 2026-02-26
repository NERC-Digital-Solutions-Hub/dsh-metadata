# Experimental Design/Sampling Regime

- Purpose: Use simulated landscape data to demonstrate environmental condition and ecosystem service (hydrological mitigation) provision in a consistent, comparable format, supporting monitoring of environmental health and policy performance over time.
- Context for analysts: Applies standardised, transparent methods to generate, verify, and transform data for monitoring dashboards, reports, and maps.

## Datasets Generated

- Output_SummaryHiraethlyn.csv
  - Configuration: 100 simulated landscapes for the Hiraethlyn sub-catchment.
  - Landscape design: Patch number (PN) and landscape proportion (LP) varied independently to separate effects of fragmentation from total forest area.
  - LP values: 10%, 25%, 50%, 75%.
  - PN values: 1, 2, 4, 8, 16.
  - Output focus: Upslope area of woodland patches as a proxy for hydrological mitigation (area_mitigated_sqkm).
  - Structure: 10 columns, 100 rows per run; key metrics include avgstreamdst_m, pland, pd, ed, enn_cv, np, area_mitigated_sqkm, total_edge_m, and related descriptors.
- Output_Summary_10_regions.csv
  - Configuration: 7,579 rows per 10 study regions (total > 7,000 per region; 10 regions).
  - Landscape design: LP and PN drawn randomly, producing landscapes along a continuum from 0 to 100% woodland.
  - Scope: More than 700 landscape configurations generated for each of the 10 test landscapes.
  - Output focus: Mitigation metrics (mit_per) and a broad suite of fragmentation and landscape metrics.
  - Structure: 19 columns, includes mit_per (mitigated percentage), prop_mit (mitigated proportion), upslope_area_km2, study_area metrics, stream length, drainage density, slope statistics, mean/sum stream order, std/slope/aspect, etc.

## Methodology

- Landscape generation approach
  - Hiraethlyn dataset: Systematic combinations of LP and PN to decouple effects of fragmentation from total woodland area.
  - 10_regions dataset: Randomized LP and PN, yielding landscapes from 0–100% woodland to reflect natural variability across study areas.
- Hydrological mitigation proxy
  - LUCI model applied to each virtual landscape to compute upslope area for woodland patches.
  - Mitigated area (area_mitigated_sqkm) and mitigated percentage (mit_per) serve as proxy metrics for hydrological ecosystem services.
- Tools and software
  - ArcGIS 10.5; LUCI Ecosystem Services model; LandscapeR; R Studio.
  - LandscapeR package reference: https://cran.r-project.org/web/packages/landscapeR/
  - LUCI model reference: https://www.lucitools.org/
- Spatial and data foundation
  - Conwy catchment topography derived from a 5 m Digital Terrain Model (DTM).
  - DTM sources: NextPerspectives, 2014; licensed for PGA use.
- Quality control
  - Basic consistency checks: values checked against feasible ranges; standard sense-checks of metrics.

## Data Structure and Variables (Overview)

- Output_SummaryHiraethlyn.csv
  - 10 columns; 100 iterations.
  - Key variables (examples): avgstreamdst_m (mean overland flow distance to stream), pland (landscape proportion), pd (patch density), ed (edge density), enn_cv (coefficient of variation of Euclidean nearest-neighbour distance), np (number of patches), plandf (landscape proportion as a categorical/factor), area_mitigated_sqkm (mitigated area), total_edge_m (total patch edge length).
- Output_Summary_10_regions.csv
  - 19 columns; 7,579 rows per region; 10 regions.
  - Key variables (examples): mit_per (mitigated percentage), prop_mit (mitigated proportion), upslope_area_km2, study_area_m2/km2, streamlength_m, draindensitym_m2/km2, max_slope/std_slope/mean_slope, meanstreamorder/sumstreamorder, std_aspect.

## Practical Implications for Analysts

- Enables decomposition of fragmentation effects from total woodland area on hydrological mitigation.
- Provides standardised outputs suitable for monitoring environmental health and policy performance over time.
- Datasets are designed for reuse and sharing within environmental monitoring portals, with clear provenance and metadata in the data structure descriptions.
- Outputs can be linked to regional planning and woodland management strategies by comparing mit_per/area_mitigated_sqkm across LP and PN configurations and across study regions.

## References and Access

- LandscapeR package: https://cran.r-project.org/web/packages/landscapeR/
- LUCI model: https://www.lucitools.org/
- Conwy catchment topography and 5 m DTM: NextPerspectives, 2014 (licensed use)