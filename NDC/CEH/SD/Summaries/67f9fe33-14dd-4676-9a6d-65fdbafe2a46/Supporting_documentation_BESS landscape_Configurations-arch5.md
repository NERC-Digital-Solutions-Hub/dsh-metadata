# Experimental Design/Sampling Regime

- Purpose and scope
  - Describes theoretical analyses using simulated landscapes to assess hydrological mitigation via upslope area.
  - Two datasets are generated and documented: Output_SummaryHiraethlyn and Output_Summary_10_regions.

- Datasets described
  - Output_SummaryHiraethlyn.csv
    - 10 columns, 100 rows.
    - Key variables include: avgstreamdst_m (mean overland flow distance to stream), pland (landscape proportion), pd (patch density), ed (edge density), enn_cv (Euclidean nearest-neighbour distance CV), np (number of patches), area_mitigated_sqkm (mitigated area), total_edge_m (total patch perimeter), plus iteration.
  - Output_Summary_10_regions.csv
    - 19 columns, 7,579 rows.
    - Key variables include: mit_per (mitigated percentage), prop_mit (mitigated proportion), upslope_area_km2, study_areaid, study_area_m2/km2, streamlength_m, draindensitym_m2/km2, max_slope, std_slope, mean_slope, meanstreamorder, sumstreamorder, std_aspect, among others.

- Landscape generation and experimental design
  - Output_SummaryHiraethlyn
    - 100 simulated landscape configurations for a single sub-catchment.
    - Patch configurations created by varying proportion woodland (LP) at 10%, 25%, 50%, 75% and number of patches (PN) at 1, 2, 4, 8, 16.
    - Purpose: disentangle effects of fragmentation vs. total forest area.
  - Output_Summary_10_regions
    - Ten sub-landscapes (Conwy catchment) with landscapes generated across random numbers of patches and woodland cover (0–100%), generating over 700 configurations per landscape.
    - No pre-set LP/PN; landscapes fall along a continuum of woodland coverage.

- Analytical methods and metrics
  - LUCI model applied to each virtual landscape to compute upslope area for woodland patches.
  - Primary dependent metric: mitigated area (area_mitigated_sqkm or mit_per/prop_mit as variants) reflecting hydrological mitigation.
  - Additional metrics capture landscape structure and context: edge density, patch density, landscape proportion, drainage density, slopes, and stream order metrics.

- Tools and software
  - ArcGIS 10.5
  - LUCI Ecosystem Services model
  - LandscapeR (R package)
  - R Studio

- Data structure and units
  - Output_SummaryHiraethlyn.csv
    - 10 columns with defined units (see variable descriptions in the dataset details; examples include meters for distances, percentages for proportions, and square-kilometers for area).
  - Output_Summary_10_regions.csv
    - 19 columns with defined units (e.g., percentages for mitigated measures, meters and meters per cell for edge metrics, km2 for areas, degrees for slope-related metrics).

- Quality control and provenance
  - Basic sense-checks performed to ensure metric values fall within feasible ranges.
  - Data provenance notes:
    - LandscapeR package: https://cran.r-project.org/web/packages/landscapeR/
    - LUCI model information: https://www.lucitools.org/
    - Conwy catchment topography derived from 5m Digital Terrain Model (NextPerspectives, 2014; licensed to NERC CEH for PGA).

- Metadata and governance considerations for data stewards
  - Clear documentation of dataset purpose, generation procedures, and variable definitions to support discoverability and reuse.
  - Reproducibility supported by explicit methodological steps (landscape generation rules, LUCI application, and data structure details).
  - Licensing and provenance information provided for tools and input data (DTM source and licensing).