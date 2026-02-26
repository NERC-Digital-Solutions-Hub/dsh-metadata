# ManagementYieldSoilVegetationData2019.csv

- Purpose and scope
  - A dataset from Sabah, Malaysian Borneo, collected Aug–Nov 2019.
  - Examines variation in yield on smallholder oil palm farms and the role of management intensity, ground vegetation cover, and soil characteristics (SOC, total N, total P, available P) on yields.
  - Data gathered from 40 smallholdings (<50 ha) across six governance areas.
  - Data collection methods: face-to-face farmer interviews for management practices (including Best Management Practices, BMPs) and reported Fresh Fruit Bunch (FFB) yields; field surveys to quantify vegetation cover and soil chemical properties; all farms had mature oil palm trees (>8 years).

- Data structure and coverage
  - Four CSV files in the dataset:
    - ManagementYieldSoilVegetationData2019.csv
    - raw_vegetationPlot2019.csv
    - raw_vegetationQuadrat2019.csv
    - raw_vegetationTransect2019.csv
  - Each file contributes different layers of information: farm-level management and yield, plot-level understorey data, quadrat-level vegetation measurements, and transect-level palm characteristics.

- Key contents by file

  - ManagementYieldSoilVegetationData2019.csv
    - 37 columns combining:
      - Farm information (e.g., plot_id, region, productiveTrees, farmArea_total, topography, monoculture, average_crop_age, previous_landuse, numb_cropCycle).
      - Management intensity index variables (e.g., pruning_freq, contour, weed_freq, herbicide_freq, herbicide_use, herbicide_perha, fertiliser_perha, fertiliser_freq, fertiliser_use, fertiliser_per_ha_yr, insecticide_use).
      - Best Management Practices (BMPs) information (e.g., EFB_application, spraying pattern).
      - Yield data (e.g., yield_per_ha_yr, yield_per_tree_yr, harvest_freq).
      - Soil chemical properties (SOC, nitrogen_total, carbon_total, phosphorus_total, phosphorus_available, and related corrections).
      - Understorey vegetation cover data (principal_component_1, principal_component_2, used for summarizing vegetation structure).
    - Purpose: supports analyses linking yield to management intensity, BMPs, soil properties, and understorey vegetation.

  - raw_vegetationPlot2019.csv
    - 9 columns:
      - plot_id, start_date, large_trees, small_trees, sapling_count, palm_count, wild_palm, standing_deadwood, understorey_density.
    - Methods: per-plot measurements including understorey density (4 measurements around the plot center, averaged), counts of non-palm trees by size classes, standing deadwood.
    - Purpose: characterise plot-level vegetation structure and diversity contributing to yield context.

  - raw_vegetationQuadrat2019.csv
    - 12 columns:
      - plot_id, start_date, quadrat_numb, canopy_height, vegetation_height, densiometer, canopy_cover, leaflitter_depth, common_name, cover_species, percentage_cover.
    - Methods: eight 1 m × 2 m quadrats per plot placed at random bearings 25 m from the center; recorded understorey height, vegetation height, leaf litter depth, canopy openness (densiometer), canopy_cover, substrate/vegetation categories, and species-specific cover data.
    - Purpose: detailed, localized characterization of ground and understory vegetation structure and composition.

  - raw_vegetationTransect2019.csv
    - 7 columns:
      - plot_id, tree_height, diameter_DBH, epiphyte_cover, contour_presence, tree_sex.
    - Methods: 60 m transect through plot center (north–south); for each oil palm tree within 5 m of transect, recorded palm height, DBH, epiphyte cover on trunk, vegetation within 2 m around palm base, and palm sex (male/female).
    - Purpose: capture tree-level structure and epiphytic/ground vegetation context around palms along transects.

- Soil sampling and laboratory analysis
  - In each 0.28 ha plot, soil samples (0–20 cm) collected from four locations to capture spatial variability:
    - near palm, near stacked frond piles, on the path, and between two palms along planting row.
  - Samples combined to one per farm; prepared and analysed for:
    - pH, total organic carbon (SOC), total carbon (C), nitrogen (N), phosphorus (P), available phosphorus (available P).
  - Analytical methods:
    - SOC: rapid dichromate oxidation (Nelson and Sommers 1982).
    - Total C and total N: dry combustion.
    - Available P: Bray and Kurtz (1945) colorimetry.
    - Total P: sulfuric acid–hydrogen peroxide method with colorimetry.
  - Results corrected to oven-dry basis.

- Understorey vegetation measures and PCA
  - Principal components (principal_component_1 and principal_component_2) derived from a PCA on 18 vegetation parameters to summarize understorey structure and diversity.
  - Data used for PCA were drawn from raw_vegetationPlot2019.csv, raw_vegetationQuadrat2019.csv, and raw_vegetationTransect2019.csv.

- Data collection methodology
  - Interviews conducted in Bahasa Malay using standardized close-ended questions to capture yield, management practices, BMPs, and farm characteristics.
  - Field sampling included plot-level vegetation surveys, quadrat-based ground vegetation assessments, and transect-based palm measurements.
  - All farms had mature oil palm trees (>8 years).

- Data use and potential outputs for data support
  - Facilitates self-serve analyses and dashboards linking management intensity, BMP adoption, soil properties, and yield outcomes.
  - Supports exploration of how understorey vegetation structure (via PCA components) relates to yield and management practices.
  - Useful for cross-file data joins by plot_id to build multivariate models of yield drivers, identify data gaps, and inform data quality improvements across diverse data formats and collection methods.

- Practical considerations for data users
  - Four-file dataset with both farm-level and plot-level measurements; careful alignment by plot_id and start_date when integrating.
  - Acknowledge spatial heterogeneity in soils and vegetation; soil samples are combined per farm, which may limit micro-site resolution.
  - PCA-derived components provide condensed understorey information but require interpretation within the broader management and soil context.