# ManagementYieldSoilVegetationData2019.csv

- Purpose and scope
  - Investigates variation in yield on smallholder oil palm farms and the role of management intensity, ground vegetation cover, and soil characteristics (SOC, total N, total P, available P) on yields.
  - Data collected Aug–Nov 2019 from 40 smallholdings (<50 ha) across six governance areas in Sabah, Malaysia.
  - Combines farmer-reported management practices (via face-to-face questionnaires) with field measurements of vegetation and soil; all farms had oil palm trees >8 years old.

- Data files included
  - ManagementYieldSoilVegetationData2019.csv
  - raw_vegetationPlot2019.csv
  - raw_vegetationQuadrat2019.csv
  - raw_vegetationTransect2019.csv

- Data structure and key content
  - First file (37 columns) organized into:
    - Farm characteristics
    - Variables for calculating a management intensity index
    - Best Management Practices (BMPs)
    - Fresh Fruit Bunch (FFB) yield data
    - Soil chemical properties
    - Understorey vegetation cover
  - Farm information fields (examples)
    - plot_id, region, productiveTrees, productiveTrees_ha, productiveTree_area
    - numb_cropCycle, monoculture, average_crop_age
    - previous_landuse, topography, farmArea_total
  - Management intensity index variables
    - pruning_freq, contour, weed_freq, herbicide_freq, herbicide_use, herbicide_perha, herbicide_per_ha_yr
    - fertiliser_use, fertiliser_freq, fertiliser_perha, fertiliser_per_ha_yr, fertiliser_pertree
    - fertiliser_per_ha_yr, insecticide_use
  - BMP variables
    - EFB_application, Spraying pattern
  - Yield-related variables
    - harvest_freq, yield_per_ha_yr (tonnes/ha), yield_per_ha_yr (kg/tree)
  - Soil data fields
    - organicCarbon_total, nitrogen_total, carbon_total, phosphorus_available, phosphorus_total
  - Understorey vegetation data
    - principal_component_1, principal_component_2 (PCA components)
  - Raw vegetation data files details
    - raw_vegetationPlot2019.csv: plot-level understorey density, standing_deadwood, non-palm trees by size classes, palm seedlings
    - raw_vegetationQuadrat2019.csv: eight 1 m x 1 m quadrats per plot; canopy height, understory height, vegetation height, leaf litter depth, densiometer readings, canopy_cover, substrate cover types, percentage_cover
    - raw_vegetationTransect2019.csv: 60 m transect; for oil palms within 5 m of transect line: tree_height, diameter_DBH, contour_cover, tree_sex

- Data collection and methods
  - Farmer interviews
    - Face-to-face interviews in Bahasa Melayu using standardized close-ended questions to capture yield, management practices, and BMP adoption.
  - Soil sampling and laboratory analysis
    - In each 0.28 ha plot, composite soil sample from four sub-locations (2 m from a palm, near frond piles, on path, between palms).
    - Soil processing: air-dried, ground, and analysed for SOC, total C and N, available P (Bray and Kurtz), total P; moisture content; analyses performed by Sabah Forest Research Centre.
  - Understorey vegetation data
    - PCA-based reduction to principal_component_1 and principal_component_2 using 18 vegetation parameters from raw files.
  - Vegetation measurements (plots)
    - Eight random 1 m x 1 m quadrats per plot at ~25 m from center; recorded canopy height, understory height, leaf litter depth, canopy openness (densiometer), and substrate/vegetation cover types with percentage cover.
  - Transect measurements
    - 60 m north-south transect through each plot; for oil palm trees within 5 m: percentage canopy vegetation around palm base, epiphyte cover on trunk, tree height, DBH, and palm sex.

- Data quality, metadata and governance implications
  - Comprehensive, multi-faceted dataset linking management practices to yields, soil health, and vegetation structure.
  - Includes metadata on variable definitions, measurement methods, and units to support reproducibility and policy-relevant monitoring.
  - Potential governance considerations for monitoring frameworks include ensuring data accessibility, timeliness, consistent metadata, and standardised data sharing to overcome silos and support transparent decision-making.

- Utility for policy and monitoring
  - Enables evaluation of how management intensity and BMP adoption influence yields and soil health in smallholder oil palm systems.
  - Supports development and refinement of monitoring indicators (e.g., BMP uptake, soil fertility indicators, understorey diversity) and informs policy decisions to enhance sustainable yield.
  - Provides a basis for cross-site comparison within Sabah and for tracking changes over time if repeated in future surveys.