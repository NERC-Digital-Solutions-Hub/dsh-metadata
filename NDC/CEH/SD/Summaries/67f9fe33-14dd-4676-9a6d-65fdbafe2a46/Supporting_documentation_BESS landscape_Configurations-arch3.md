# Experimental Design/Sampling Regime

- Purpose: Describe the experimental design used to assess hydrological mitigation provided by woodland patches and improved grassland, via simulated landscapes and the LUCI ecosystem services model; datasets are intended to inform evaluation of landscape configuration effects on environmental health metrics.

- Datasets overview:
  - Output_SummaryHiraethlyn.csv: 100 landscape configurations for the Hiraethlyn sub-catchment (10%–75% woodland proportion LP; 1,2,4,8,16 patches PN). All combinations created to separate fragmentation effects from forest area.
  - Output_Summary_10_regions.csv: 10 sub-landscapes in the Conwy catchment with random LP and PN, generating over 7,500 rows per study area; landscapes span a continuum from 0–100% woodland.

- Landscape generation approach:
  - Hiraethlyn: 100 configurations across all LP and PN combinations; patches allocated randomly up to user-defined patch numbers.
  - 10_regions: Landscapes with random numbers of patches and woodland proportion; broad coverage along a woodland-coverage continuum.

- Modelling and proxy metric:
  - LUCI model used to calculate upslope area for each woodland patch.
  - Proxy metric: area_mitigated_sqkm (Hiraethlyn) and mit_per / prop_mit (10_regions) representing hydrological mitigation provided by patches.

- Fieldwork/Instrumented tools and software:
  - ArcGIS 10.5
  - LUCI Ecosystem Services model
  - LandscapeR (R package)
  - R Studio
  - LandscapeR and LUCI resources referenced for methodology and implementation

- Data structure and variables:
  - Output_SummaryHiraethlyn.csv:
    - iteration: run number (1–100)
    - avgstreamdst_m: mean overland distance from patch to stream (m)
    - pland: landscape proportion of woodland (percent)
    - pd: patch density (patches per landscape area)
    - ed: edge density (edge length per landscape area; m per cell)
    - enn_cv: coefficient of variation of Euclidean nearest-neighbour distance (m)
    - np: number of patches
    - plandf: landscape proportion as a factor
    - area_mitigated_sqkm: mitigated area (km^2)
    - total_edge_m: total edge length (m)
  - Output_Summary_10_regions.csv:
    - mit_per: mitigated percentage (percent)
    - ed, pd, pland: fragmentation, patch density, woodland proportion
    - prop_mit: mitigated proportion (fraction)
    - upslope_area_km2: upslope area (km^2)
    - study_areaid / study_area_m2 / study_area_km2: region identifiers and area
    - streamlength_m: total stream length (m)
    - draindensitym_m2 / draindensitykm_km2: drainage density metrics
    - max_slope / std_slope / mean_slope: slope statistics (degrees)
    - meanstreamorder / sumstreamorder: Strahler order metrics
    - std_aspect: standard deviation of aspect (degrees)
  - Miscellaneous notes: dataset details include units, data structure descriptions, and run iterations (1–100)

- Data quality and governance:
  - Quality control: standard sense checks of metrics (values within feasible ranges).
  - Metadata and data sharing: metadata exist within dataset descriptions; public sharing of underlying data can be a barrier in some contexts; data provenance and governance emphasized.
  - Data provenance and reproducibility: LUCI model, ArcGIS workflow, and R-based analyses are documented; outputs are presented in clear tabular formats for reproducibility.

- Accessibility and potential barriers:
  - Data access may be restricted by metadata gaps, data sharing policies, or institutional barriers.
  - Fragmentation and governance barriers (silos) can hinder sharing and reuse of datasets across organisations.

- Miscellaneous context:
  - LandscapeR package and LUCI model links provided for further reference.
  - Conwy catchment topography derived from a 5m Digital Terrain Model (NextPerspectives).