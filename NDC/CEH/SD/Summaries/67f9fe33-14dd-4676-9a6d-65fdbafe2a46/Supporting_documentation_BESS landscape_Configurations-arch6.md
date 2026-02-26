# Experimental Design/Sampling Regime

- Overview: Describes two landscape-generation experiments and the resulting datasets, using the LUCI model to estimate a hydrological mitigation proxy (upslope area) for woodland patches.

- Experimental setup
  - Output_SummaryHiraethlyn.csv
    - 100 simulated landscape configurations for the Hiraethlyn sub-catchment.
    - Patch numbers (PN): 1, 2, 4, 8, 16.
    - Landscape proportion (LP): 10%, 25%, 50%, 75%.
    - Patches allocated randomly to separate fragmentation effects from forest area.
  - Output_Summary_10_regions.csv
    - 10 sub-landscapes within the Conwy catchment; landscapes generated for each test area with random numbers of patches and woodland cover.
    - >700 configurations per region; landscapes span a continuum from 0–100% woodland.
    - Objective: capture a wide landscape configuration space across multiple study areas.

- Analytical approach
  - LUCI model applied to each virtual landscape to calculate upslope area for woodland patches.
  - Upslope area (total) used as a proxy metric for hydrological mitigation ecosystem services.

- Tools and workflow
  - ArcGIS 10.5, LUCI Ecosystem Services model, LandscapeR, R Studio.

- Data structure and contents
  - Output_SummaryHiraethlyn.csv
    - 10 columns, 100 rows.
    - Key variables (with units): avgstreamdst_m (mean overland flow distance from patch to stream, m); pland (landscape proportion, %); pd (patch density, patches per landscape area, unitless); ed (edge density, m per cell); enn_cv (Euclidean nearest-neighbour distance CV, m); np (number of patches, unitless); plandf (landscape proportion as a factor, unitless); area_mitigated_sqkm (mitigated area, km^2); total_edge_m (total edge length, m).
  - Output_Summary_10_regions.csv
    - 19 columns, 7,579 rows.
    - Key variables (with units): mit_per (mitigated percentage, %); ed (edge density, m per cell); pd (patch density, unitless); pland (landscape proportion, % or unitless as defined); prop_mit (mitigated proportion, unitless); upslope_area_km2 (upslope area, km^2); study_areaid (region identifier, unitless); study_area_m2 (area of study region, m^2); study_area_km2 (area of study region, km^2); streamlength_m (total stream length, m); draindensitym_m2 (drainage density, m/m^2); draindensitykm_km2 (drainage density, m/km^2); max_slope (maximum slope, degrees); std_slope (standard deviation of slope, degrees); mean_slope (mean slope, degrees); meanstreamorder (mean Strahler order, unitless); sumstreamorder (sum Strahler order, unitless); std_aspect (std dev of aspect, degrees from North).
  - Data quality: Includes standard sense checks; units are specified per variable in the data structure detail.

- Data provenance and references
  - LandscapeR package: https://cran.r-project.org/web/packages/landscapeR/
  - LUCI model information: https://www.lucitools.org/
  - Conwy catchment topography derived from a 5m Digital Terrain Model (DTM); licensing note included.