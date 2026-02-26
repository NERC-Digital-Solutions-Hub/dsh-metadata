# Experimental Design/Sampling Regime

- The document outlines a theoretical analysis using simulated landscapes (no field or lab experiments) to study hydrological mitigation via woodland patches.
- Two datasets are generated and analysed to separate effects of fragmentation from total forest area.

## Experimental design and data generation

- Output_SummaryHiraethlyn
  - Generates 100 simulated landscape configurations for the Hiraethlyn sub-catchment.
  - Patches allocated randomly up to a user-defined number of patches (PN) and area of coverage (LP).
  - LP levels: 10%, 25%, 50%, 75%.
  - PN values: 1, 2, 4, 8, 16.
  - Purpose: separate impacts of fragmentation per se from total forest area.

- Output_Summary_10_regions
  - Uses ten sub-landscapes in the Conwy catchment.
  - Landscape generation with random numbers of patches and woodland coverage, spanning 0–100% woodland.
  - Over 700 landscape configurations generated for each test area.

- Both datasets
  - LUCI ecosystem services model applied to each virtual landscape to calculate upslope area for each woodland patch.
  - Total upslope area used as a proxy for hydrological mitigation (mitigated area).

## Datasets and data structure

- Software and workflow
  - ArcGIS 10.5, LUCI model, LandscapeR, R Studio.
  - LUCI and LandscapeR resources cited; Conwy topography from a 5 m Digital Terrain Model (DTM).

- Output_SummaryHiraethlyn.csv
  - Size: 10 columns, 100 rows.
  - Key variables (examples with units):
    - iteration (unitless)
    - avgstreamdst_m (mean distance to stream, meters)
    - pland (landscape proportion: woodland area / total landscape, %)
    - pd (patch density, patches per landscape area, unitless)
    - ed (edge density, meters per cell)
    - enn_cv (coefficient of variation of Euclidean nearest-neighbour distance, meters)
    - np (number of patches, unitless)
    - plandf (landscape proportion as a factor, unitless)
    - area_mitigated_sqkm (mitigated area after hydrological routing, square kilometers)
    - total_edge_m (total edge length, meters)

- Output_Summary_10_regions.csv
  - Size: 19 columns, 7,579 rows.
  - Key variables (examples with units):
    - mit_per (mitigated percentage, %)
    - ed (edge density, meters per cell)
    - pd (patch density, unitless)
    - pland (landscape proportion, unitless)
    - prop_mit (mitigated proportion, unitless)
    - upslope_area_km2 (upslope area, square kilometers)
    - study_areaid (region identifier, unitless)
    - study_area_m2 / study_area_km2 (area of study region, m2 / km2)
    - streamlength_m (total stream length, meters)
    - draindensitym_m2 and draindensitykm_km2 (drainage density, meters per meter squared and per square kilometer)
    - slope metrics: max_slope (degrees), std_slope (degrees), mean_slope (degrees)
    - meanstreamorder and sumstreamorder (Strahler order metrics)
    - std_aspect (standard deviation of aspect, degrees)

## Data quality, governance and provenance

- Quality control
  - Standard sense checking of metric ranges (feasible ranges).

- Metadata and discoverability
  - Detailed variable descriptions and units are documented within each dataset structure.
  - Data sources and tools clearly cited (ArcGIS, LUCI, LandscapeR, R Studio).
  - Topographic and regional context documented (Conwy catchment, 5 m DTM; NextPerspectives license).

- Reproducibility and usage
  - Scripted landscape generation linked to explicit LP and PN parameter combinations.
  - Outputs provide explicit metrics for comparison of fragmentation vs. forest area effects on hydrological mitigation.
  - Access to tools and model references provided for replication (LandscapeR and LUCI websites).

## Implications for data strategy and practice

- The datasets exemplify how to design data assets that:
  - Capture controlled experimental variations (fragmentation vs. area) to isolate effects.
  - Produce rich, multi-metric outputs suitable for policy-relevant analysis (mitigation benefits, fragmentation indicators, and landscape structure statistics).
  - Include clear provenance, processing steps, and metadata to support discoverability and reuse.
- Data Leaders can use this as a model for:
  - Documenting dataset structure, variables, and units for internal governance.
  - Ensuring reproducible workflows across different study regions and scenarios.
  - Aligning data collection and modeling efforts with user needs and downstream dissemination.