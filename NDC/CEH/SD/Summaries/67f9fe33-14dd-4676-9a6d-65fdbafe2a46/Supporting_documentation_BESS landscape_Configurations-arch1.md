# Experimental Design/Sampling Regime

- Purpose and approach
  - Develop and analyze simulated landscape configurations to understand how woodland patch fragmentation and total woodland area influence hydrological mitigation services.
  - Apply a consistent modeling workflow (LUCI) to generate a proxy metric of mitigation and to compare different landscape scenarios.

- Datasets generated
  - Output_SummaryHiraethlyn.csv
    - 100 landscape iterations for the Hiraethlyn sub-catchment.
    - Landscape proportions (LP) and patch numbers (PN) configured as: LP = 10, 25, 50, 75% and PN = 1, 2, 4, 8, 16.
    - Purpose: separate effects of fragmentation from total woodland area.
    - Variables (10 total, per row): average overland distance to stream (avgstreamdst_m), landscape proportion (pland), patch density (pd), edge density (ed), Euclidean nearest-neighbour distance metrics (enn_cv), number of patches (np), landscape proportion as a factor (plandf), mitigated area (area_mitigated_sqkm), total edge (total_edge_m).
  - Output_Summary_10_regions.csv
    - >7,000 rows (7,579) across ten sub-regions; landscapes generated with random patch counts and a continuum of woodland from 0–100%.
    - For each study region, outputs include: mitigated percentage (mit_per), edge density (ed), patch density (pd), landscape proportion (pland), mitigated proportion (prop_mit), upslope area (upslope_area_km2), study area identifiers and area metrics, stream length (streamlength_m), drainage densities (draindensitym_m2, draindensitykm_km2), and slope/aspect metrics (max_slope, std_slope, mean_slope, meanstreamorder, sumstreamorder, std_aspect).

- Landscape generation details
  - Hiraethlyn: 100 configurations per LP/PN combination; LP set at 10, 25, 50, 75%; PN at 1, 2, 4, 8, 16.
  - Conwy (10 regions): landscapes created with random numbers of patches; distribution spans 0–100% woodland; over 700 configurations per test area.

- Modeling and metrics
  - LUCI model applied to each virtual landscape to compute upslope area for woodland patches.
  - Upslope area (sum of upslope areas) used as a proxy for hydrological mitigation services.

- Tools and software
  - ArcGIS 10.5
  - LUCI Ecosystem Services model
  - LandscapeR
  - R Studio

- Calibration and quality control
  - Calibration steps: not applicable (N/A)
  - Quality control: standard plausibility checks of metrics within feasible ranges

- Data structure and documentation
  - Output_SummaryHiraethlyn.csv: 10 variables; 100 iterations; units provided in the dataset details.
  - Output_Summary_10_regions.csv: 19 variables; 7,579 rows; units provided in the dataset details.
  - Detailed variable descriptions and units are documented in the respective data structure sections.

- Miscellaneous and data provenance
  - LandscapeR package: https://cran.r-project.org/web/packages/landscapeR/
  - LUCI model information: https://www.lucitools.org/
  - Conwy catchment topography derived from a 5m Digital Terrain Model (NextPerspectives, 2014) licensed for PGA through Next Perspectives.