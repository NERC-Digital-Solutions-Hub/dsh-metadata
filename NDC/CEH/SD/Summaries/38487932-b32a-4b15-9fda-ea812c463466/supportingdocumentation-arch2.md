# ManagementYieldSoilVegetationData2019.csv

## Aim
- Examine variation in yield on smallholder oil palm farms and the roles of management intensity, ground vegetation cover, and soil characteristics (SOC, total N, total P, available P) on yields.
- Data collected Aug–Nov 2019 from 40 smallholdings (<50 ha) across six governance areas in Sabah, Malaysia.
- Include farmer-reported Fresh Fruit Bunch (FFB) yields, BMPs, and field-measured vegetation and soil properties to support assessment of environmental health and policy performance over time.

## Data collection scope and context
- Farm type: smallholder oil palm farms with mature trees (>8 years).
- Methods: face-to-face interviews (Bahasa Malay) using standardized close-ended questions; accompanying field surveys for vegetation and soil measurements.
- Purpose: quantify management practices, environmental variables, and yields to enable standardized monitoring and analysis.

## Data structure and files
- Four CSV files in the dataset:
  - ManagementYieldSoilVegetationData2019.csv
  - raw_vegetationPlot2019.csv
  - raw_vegetationQuadrat2019.csv
  - raw_vegetationTransect2019.csv

## Dataset composition: ManagementYieldSoilVegetationData2019.csv (37 columns)
- Farm information (examples):
  - plot_id, region, productiveTrees, productiveTrees_ha, productiveTree_area, numb_cropCycle, monoculture, average_crop_age, previous_landuse, topography, farmArea_total
- Variables for management intensity index:
  - pruning_freq, contour, weed_freq, herbicide_freq, herbicide_use, herbicide_perha, herbicide_per_ha_yr, fertiliser_perha, fertiliser_pertree, fertiliser_freq, fertiliser_use, fertiliser_per_ha_yr, insecticide_use
- Best Management Practices (BMPs):
  - EFB_application, Spraying pattern
- Yield data:
  - harvest_freq, yield_per_ha_yr (t/ha), yield_per_tree_kg
- Soil chemical properties:
  - organicCarbon_total, nitrogen_total, carbon_total, phosphorus_available, phosphorus_total
- Understorey vegetation:
  - principal_component_1, principal_component_2

## Raw vegetation data files
- raw_vegetationPlot2019.csv (9 columns)
  - plot_id, start_date, large_trees, small_trees, sapling_count, palm_count, wild_palm, standing_deadwood, understorey_density
- raw_vegetationQuadrat2019.csv (12 columns)
  - plot_id, start_date, quadrat_numb, canopy_height, vegetation_height, densiometer, canopy_cover, leaflitter_depth, common_name, cover_species, percentage_cover
- raw_vegetationTransect2019.csv (7 columns)
  - plot_id, tree_height, diameter_DBH, epiphyte_cover, contour_presence, contour_cover, tree_sex

## Methods and data collection details
- Vegetation data collection:
  - Plot-level: eight 1 m x 1 m quadrats placed at random bearings 25 m from plot centre; measurements include understory height, vegetation height, leaf litter depth, canopy openness (densiometer), and substrate cover types.
  - Transect: 60 m transect through plot centre; for each oil palm within 5 m of transect, recorded epiphyte cover on trunks and vegetation within a 2 m radius at the palm base.
  - Understorey density: measured as an average score from four measurements (0 = low density to 1 = high density).
- Species and substrate data:
  - Common names provided (local Malay names); substrates include litter, moss, bare ground, deadwood, and various vegetation categories.
- Soil sampling and analysis:
  - In each 0.28 ha plot, four soil samples (0–20 cm depth) taken to capture spatial variability and combined into one composite sample per farm.
  - Laboratory analyses:
    - SOC (%), carbon (%), nitrogen (%): dry combustion methods
    - Available phosphorus (mg/kg): Bray and Kurtz method
    - Total phosphorus (mg/kg): sulfuric acid–hydrogen peroxide method
  - Moisture content determined by oven-drying sub-sample (105°C)
  - SOC, total C, and N corrected to oven-dry basis
  - Analyses conducted by Sabah Forest Research Centre
- Data processing:
  - Principal Component Analysis (PCA) applied to 18 vegetation parameters to derive principal_component_1 and principal_component_2, using data from raw_vegetationPlot2019.csv, raw_vegetationQuadrat2019.csv, and raw_vegetationTransect2019.csv.

## Units and record values (highlights)
- farm and plot identifiers: plot_id, start_date
- Farm characteristics: region, topography, farmArea_total, monoculture, average_crop_age
- Management and inputs: pruning_freq, weed_freq, herbicide_freq/use, fertiliser_freq/use, fertiliser_perha, fertiliser_per_ha_yr, fertiliser_pertree, herbicide_perha, herbicide_per_ha_yr, insecticide_use
- BMPs: EFB_application, Spraying pattern
- Yield: harvest_freq (per month), yield_per_ha_yr (tonnes/ha), yield_per_tree_kg
- Soil properties: organicCarbon_total (%), carbon_total (%), nitrogen_total (%), phosphorus_available (mg/kg), phosphorus_total (mg/kg)
- Vegetation and understorey: principal_component_1, principal_component_2, understorey_density, canopy_cover, leaflitter_depth, canopy_height, vegetation_height, densiometer
- Palm characteristics: tree_height (m), diameter_DBH (cm), epiphyte_cover, tree_sex (male/female), contour_cover

## Relevance for environmental monitoring and analysis
- Standardized, linked dataset enabling cross-site comparisons of yield, management intensity, soil health, and vegetation structure on smallholder oil palm farms.
- Facilitates examination of how management practices and ecological factors influence environmental performance and crop yields over time.
- Data are organized to support integration with other datasets (via plot_id) and potential data portal deposition to enhance accessibility and reuse.

## Considerations and scope
- Timeframe: data collected in 2019 (August–November).
- Geography: Sabah, Malaysian Borneo, across six governance areas.
- Farm type constraint: mature trees (>8 years), farms generally <50 ha.
- Data rely on both farmer-reported information (BMPs, management practices) and direct field measurements (soil chemistry, vegetation structure).