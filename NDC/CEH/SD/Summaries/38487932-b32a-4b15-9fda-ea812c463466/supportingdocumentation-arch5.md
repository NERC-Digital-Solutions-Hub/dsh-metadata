# ManagementYieldSoilVegetationData2019

## Overview
- A study of variation in oil palm yield on smallholder farms and the influence of management intensity, ground vegetation cover, and soil properties (SOC, total N, total P, available P) on yields.
- Data collection period: August–November 2019.
- Location: Sabah, Malaysian Borneo; 40 smallholdings (<50 ha) across six governance areas.
- Data sources: face-to-face farmer interviews (BMPs and FFB yields) and field surveys for vegetation and soil properties.
- Farm maturity: all smallholders had trees that were >8 years old.

## Data files
- Four CSV files:
  - ManagementYieldSoilVegetationData2019.csv
  - raw_vegetationPlot2019.csv
  - raw_vegetationQuadrat2019.csv
  - raw_vegetationTransect2019.csv

## Data structure and key fields
- First CSV: 37 columns, spanning:
  - Farm information (e.g., plot_id, region, productiveTrees, productiveTrees_ha, productiveTree_area, numb_cropCycle, monoculture, average_crop_age, previous_landuse, topography, farmArea_total)
  - Management intensity index variables (e.g., pruning_freq, contour, weed_freq, herbicide_freq, herbicide_use, herbicide_perha, herbicide_per_ha_yr, fertiliser_perha, fertiliser_pertree, fertiliser_freq, fertiliser_use, fertiliser_per_ha_yr, insecticide_use)
  - Best Management Practices (BMPs) indicators (e.g., EFB_application, Spraying pattern)
  - Yield data (e.g., harvest_freq, yield_per_ha_yr)
  - Soil chemical properties (e.g., organicCarbon_total, nitrogen_total, carbon_total, phosphorus_available, phosphorus_total)
  - Understorey vegetation components (e.g., principal_component_1, principal_component_2)
- Second CSV (raw_vegetationPlot2019.csv): 9 columns
  - plot_id, start_date, large_trees, small_trees, sapling_count, palm_count, wild_palm, standing_deadwood, understorey_density
- Third CSV (raw_vegetationQuadrat2019.csv): 12 columns
  - plot_id, start_date, quadrat_numb, canopy_height, vegetation_height, densiometer, canopy_cover, leaflitter_depth, common_name, cover_species, percentage_cover
- Fourth CSV (raw_vegetationTransect2019.csv): 7 columns (as listed)
  - plot_id, tree_height, diameter_DBH, epiphyte_cover, contour_presence, tree_sex, [additional column not explicitly listed in the text]
- Cross-linking key: plot_id ties records across all files.

## Data collection methods
- Farm surveys:
  - Face-to-face interviews with farmers using a standardized Bahasa Malay questionnaire to capture yield data and management practices.
- Vegetation and biodiversity measurements:
  - Within each plot: eight 1 m2 quadrats placed at random bearings 25 m from plot centre to assess understorey vegetation variables (11 recorded variables including understorey height, leaf litter depth, canopy openness, substrate covers, etc.).
  - Quadrat measurements included canopy_height, vegetation_height, leaf_litter_depth, densiometer readings for canopy openness, and percentage cover for substrates (leaf litter, moss, bare ground, deadwood, ground vegetation of varying heights, etc.).
- Understorey and palm dynamics:
  - 60 m transect through plot centre (N–S). For palms within 5 m of the transect: recorded trunk epiphyte_cover and vegetation cover within a 2 m radius at the palm base; tree_height, diameter_DBH, and tree_sex noted.
- Plot sampling locations for soil:
  - Each 0.28 ha plot: four soil samples (within 2 m of a palm, near frond piles, on path, and between palms) combined into one sample per farm, depth 20 cm.

## Laboratory analysis and calculations
- Soil analysis (performed by Sabah Forest Research Centre):
  - pH, soil organic carbon (SOC) via rapid dichromate oxidation (Nelson & Sommers 1982)
  - Total carbon (C) and total nitrogen (N) via dry combustion
  - Available phosphorus (P) via Bray and Kurtz (1945) method; total P via sulphuric acid–hydrogen peroxide method with colorimetric detection
  - Moisture content by oven-drying at 105°C
  - Results corrected to oven-dry basis
- Vegetation data processing:
  - Principal Component Analysis (PCA) applied to 18 vegetation parameters across raw_vegetationPlot2019.csv, raw_vegetationQuadrat2019.csv, and raw_vegetationTransect2019.csv to derive principal_component_1 and principal_component_2 (measures of ground vegetation cover and non-palm tree diversity, respectively).

## Data governance, quality, and stewardship
- The dataset provides detailed metadata on variables, units, sampling design, and analytical methods, enabling reproducibility and data quality assessment.
- Cross-file consistency is maintained via the plot_id key; documentation includes the context of measurements and processing (e.g., PCA derivation, lab methods).
- Data stewardship considerations for reuse:
  - Clear definitions of measurement methods and units support interoperability and meta-analysis across studies.
  - Documentation of potential limitations (e.g., sampling within 0.28 ha plots, single-time-point sampling, possible variability in farmer-reported BMPs) should be considered when modeling yield.
  - Ensure alignment of any derived variables (e.g., principal_component_1/2) with their PCA methodology when integrating with other datasets.

## Practical considerations for use
- Potential analyses:
  - Modeling yield per ha or per tree as a function of management intensity, BMP adoption, soil properties, and understorey vegetation structure.
  - Exploring relationships between BMPs and soil/vegetation indicators.
- Data integration notes:
  - Use plot_id to join farm characteristics, yield, BMPs, soil properties, and vegetation measurements across the four CSVs.
  - Be mindful of units (e.g., tonnes per ha, kg per tree, cm measurements, percentages) and the date range (August–November 2019) when comparing with other datasets.
- Limitations and caveats:
  - Field measurements are cross-sectional within a single season; temporal variation beyond the study period is not captured.
  - Some columns described may have naming inconsistencies in the text (e.g., the transect file’s column count vs. listing), so users should validate column names against the actual files during import.

## Provenance and context
- Geography: Sabah, Malaysian Borneo.
- Institutions: Sabah Forest Research Centre contributed to laboratory analyses.
- Scope: 40 smallholder farms with diverse management practices and land-use histories, enabling examination of how management, soil properties, and understorey vegetation relate to yield.