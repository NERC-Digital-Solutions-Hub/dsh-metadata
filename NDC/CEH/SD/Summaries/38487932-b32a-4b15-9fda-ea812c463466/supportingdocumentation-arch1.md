# ManagementYieldSoilVegetationData2019

- This dataset captures variation in oil palm yield on smallholder farms and the roles of management intensity, ground vegetation cover, and soil characteristics (SOC, total N, total P, available P) on yields.
- Fieldwork was conducted August–November 2019 across 40 smallholdings (<50 ha) in Sabah, Malaysia, combining farmer interviews with on-site vegetation and soil surveys.
- The dataset supports analysis of how management practices and environmental factors relate to Fresh Fruit Bunch (FFB) yields and related soil/vegetation properties.

## Data files and general structure

- ManagementYieldSoilVegetationData2019.csv
  - 37 columns spanning: farm characteristics, variables for calculating a management intensity index, Best Management Practices (BMPs), yield information, soil chemical properties, and understorey vegetation PCA components.
- raw_vegetationPlot2019.csv
  - 9 columns capturing plot-level vegetation metrics, including understorey density.
- raw_vegetationQuadrat2019.csv
  - 12 columns detailing quadrat-level vegetation measurements (canopy height, vegetation height, densiometer readings, canopy cover, leaf litter depth, substrate/cover types, and percent cover).
- raw_vegetationTransect2019.csv
  - 7 columns describing transect-based palm and vegetation observations (palm height, diameter at breast height, epiphyte cover, vegetation around palm base, and palm sex).

## Study design and data collection

- Location and scale
  - 40 smallholder farms across six governance areas in Sabah, Malaysia.
  - Farms defined as <50 hectares; all had mature palms (>8 years since planting).
- Data collection methods
  - Face-to-face interviews in Bahasa Malay with standardized close-ended questions to capture management practices and reported yields (FFB).
  - Field surveys to quantify vegetation cover and soil chemical properties within plots.

## Farm and management variables

- Farm information (from ManagementYieldSoilVegetationData2019.csv)
  - plot_id: unique farm identification code
  - region: village/region
  - productiveTrees, productiveTrees_ha, productiveTree_area: tree counts and distribution
  - numb_cropCycle: palm crop replant cycles
  - monoculture: 1/0 indicating monoculture vs mixed system
  - average_crop_age: average age across farm area
  - previous_landuse: prior land use (forested or agricultural)
  - topography: flat, gentle, moderate, or sloping
  - farmArea_total: total farm area (hectares)

- Management intensity index (variables in ManagementYieldSoilVegetationData2019.csv)
  - pruning_freq, contour, weed_freq, herbicide_freq, herbicide_use, herbicide_perha, herbicide_per_ha_yr
  - fertiliser_perha, fertiliser_pertree, fertiliser_freq, fertiliser_use, fertiliser_per_ha_yr
  - insecticide_use

- Best Management Practices (BMPs)
  - EFB_application: use of empty fruit bunches or mulching (1/0)
  - Spraying pattern: localized vs blanket spraying

- Yield data
  - harvest_freq: harvests per month
  - yield_per_ha_yr: yield per hectare (tonnes/ha)
  - yield_per_tree: yield per tree (kilograms/tree)

## Soil data

- Soil properties collected per farm
  - organicCarbon_total (SOC, %)
  - nitrogen_total (N, %)
  - carbon_total (C, %)
  - phosphorus_available (available P, mg/kg)
  - phosphorus_total (P, mg/kg)
- Soil sampling method
  - In each 0.28 ha plot, four soil samples (at specific micro-sites) were combined into one farm-level sample (0–20 cm depth).
  - Analyses performed by Sabah Forest Research Centre:
    - SOC (%): rapid dichromate oxidation (Nelson & Sommers 1982)
    - Total C and N: dry combustion
    - Available P: Bray and Kurtz (1945)
    - Total P: sulphuric acid–H2O2 method with colorimetry

## Understorey vegetation data and PCA

- Principal components
  - principal_component_1 and principal_component_2: derived from a PCA on 18 vegetation parameters to quantify variability in understorey structure.
  - PCA inputs drawn from raw_vegetationPlot2019.csv, raw_vegetationQuadrat2019.csv, and raw_vegetationTransect2019.csv.

## Vegetation survey methods by data file

- raw_vegetationPlot2019.csv
  - plot_id, start_date, large_trees, small_trees, sapling_count, palm_count, wild_palm, standing_deadwood, understorey_density
  - Measurements capture non-palm vegetation density and palm context within the plot.
- raw_vegetationQuadrat2019.csv
  - plot_id, start_date, quadrat_numb, canopy_height, vegetation_height, densiometer, canopy_cover, leaflitter_depth, common_name, cover_species, percentage_cover
  - Eight 1 m x 2 m quadrats were placed per plot (eight randomly oriented quadrats at 25 m from center); recorded multiple understory variables and substrate covers.
- raw_vegetationTransect2019.csv
  - plot_id, tree_height, diameter_DBH, epiphyte_cover, contour_presence, tree_sex
  - A 60 m transect through the plot's center; for each oil palm tree within 5 m of the transect, recorded trunk epiphyte cover and surrounding vegetation cover; palm sex noted.

## Data characteristics and alignment considerations for analysts

- Cross-dataset integration
  - Core linking key is plot_id; combine ManagementYieldSoilVegetationData2019.csv with the raw vegetation and soil datasets to build models of yield as a function of management, BMP usage, soil chemistry, and understorey structure.
- Derived measures
  - Management intensity index and understorey PCA components are derived fields that can be used directly in analyses.
- Units and measurement details
  - Yields in tonnes per hectare (and kilograms per tree)
  - Soil and vegetation measurements reported with specific units as described above (e.g., SOC %, P mg/kg, canopy_height in metres, percentage_cover, etc.)

## Potential analyst applications

- Investigate relationships between management intensity, BMP adoption, and yield outcomes.
- Examine how soil chemical properties relate to yield and whether understorey structure mediates those relationships.
- Use PCA-derived understorey components to assess the impact of vegetation structure on palm productivity.
- Develop and validate predictive models of yield at the farm level using a combination of management, soil, and vegetation predictors.
- Compare management practices and yields across governance areas to identify regional patterns.