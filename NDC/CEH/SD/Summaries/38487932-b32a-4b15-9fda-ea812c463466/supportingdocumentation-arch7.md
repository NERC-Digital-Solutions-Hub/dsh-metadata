# ManagementYieldSoilVegetationData2019.csv

## Overview
- A dataset from a study of smallholder oil palm farms in Sabah, Malaysia (Aug–Nov 2019).
- Objectives: examine variation in yield and the roles of management intensity, ground vegetation cover, and soil characteristics (SOC, total N, total P, available P) on yields.
- Scope: 40 smallholdings (<50 ha) across six governance areas; farms have mature oil palm trees ( >8 years old).
- Data collection: face-to-face questionnaires on BMPs and Fresh Fruit Bunch (FFB) yields; field surveys quantify vegetation cover and soil properties.

## Data Files (four CSVs)
- ManagementYieldSoilVegetationData2019.csv
  - 37 columns: 
    - Farm characteristics
    - Variables to calculate a management intensity index
    - Best Management Practices (BMPs)
    - Fresh Fruit Bunch (yield) data
    - Soil chemical properties
    - Understorey vegetation cover
- raw_vegetationPlot2019.csv
  - 9 columns: plot_id, start_date, large_trees, small_trees, sapling_count, palm_count, wild_palm, standing_deadwood, understorey_density
- raw_vegetationQuadrat2019.csv
  - 12 columns: plot_id, start_date, quadrat_numb, canopy_height, vegetation_height, densiometer, canopy_cover, leaflitter_depth, common_name, cover_species, percentage_cover
- raw_vegetationTransect2019.csv
  - 7 columns: plot_id, tree_height, diameter_DBH, epiphyte_cover, contour_presence/contour_cover, tree_sex (plus related fields as applicable)

## Data Variables and Measurements

- Farm information (ManagementYieldSoilVegetationData2019.csv)
  - plot_id, region, productiveTrees, productiveTrees_ha, productiveTree_area, numb_cropCycle, monoculture, average_crop_age, previous_landuse, topography, farmArea_total
- Management intensity and agricultural practices
  - pruning_freq, contour (vegetation around a palm within 2 m: yes/no), weed_freq, herbicide_freq, herbicide_use, herbicide_perha, herbicide_per_ha_yr, fertiliser_perha, fertiliser_pertree, fertiliser_freq, fertiliser_use, fertiliser_per_ha_yr, insecticide_use
- Best Management Practices (BMPs)
  - EFB_application (mulching/bundles), spraying pattern
- Yield data
  - harvest_freq, yield_per_ha_yr (tonnes per hectare), yield_per_ha_yr (kg per tree)
- Soil data (SOC and nutrients)
  - organicCarbon_total (%), nitrogen_total (%), carbon_total (%), phosphorus_available (mg/kg), phosphorus_total (mg/kg)
- Understorey vegetation
  - principal_component_1, principal_component_2 (derived via PCA on 18 vegetation parameters)
- Understorey vegetation measures (raw)
  - From raw_vegetationPlot2019.csv: understorey_density (0–1 scale), counts of large/small non-palm trees, saplings, palms, standing_deadwood
- Quadrats and transects (raw)
  - raw_vegetationQuadrat2019.csv: canopy_height (m), vegetation_height (cm), densiometer, canopy_cover, leaflitter_depth, common_name, cover_species, percentage_cover
  - raw_vegetationTransect2019.csv: palm-tree measurements (e.g., tree_height, diameter_DBH), epiphyte_cover, contour_cover, tree_sex

## Methods and Data Collection

- Field data collection
  - 0.28 ha plots with four soil samples per farm to capture within-plot heterogeneity
  - Soil samples collected at fixed micro-locations: near palm, near stacked frond piles, on paths, and between palms; combined to single farm sample
  - Soil processing: oven-dried basis; SOC via rapid dichromate oxidation; C and N via dry combustion; available P via Bray and Kurtz; total P via acid digestion and colorimetry
- Vegetation data
  - Plot-level assessments of understorey density, standing deadwood, and non-palm tree diversity (three size classes)
  - Quadrat sampling (eight 1 m x 2 m quadrats per plot in random orientations) to capture canopy height, understorey height, leaf litter, canopy openness (densiometer), and substrate cover
  - Transect sampling (60 m transect through plot center) to record epiphyte cover on trunks, vegetation within 2 m of palm bases, and palm-tree attributes
- PCA for understorey
  - Principal component analysis on 18 vegetation parameters using data from the three vegetation files to derive principal_component_1 (ground vegetation cover) and principal_component_2 (non-palm tree diversity)

## GIS-Relevant Considerations

- Spatial scope and data integration
  - Farm-level data across six governance areas; geospatial coordinates are not provided in the files, but farm locations are identifiable via region and plot_id for potential geocoding.
  - Data can be linked across files via plot_id to create layered GIS visualizations (yield, management intensity, BMPs, soil properties, and vegetation structure).
- Potential GIS outputs
  - Map layers of yield per hectare or per tree by farm
  - Spatial patterns of soil chemical properties and organic carbon
  - Understorey vegetation structure via PCA component scores
  - Relationship of BMP implementation with yield and soil/vegetation metrics
- Data preparation needs for GIS
  - Optional geocoding of farms to obtain precise coordinates
  - Joining datasets on plot_id
  - Handling different data resolutions (plot-level vs. sub-plot/quadruple measurements)

## Quality, Limitations, and Use

- Limitations
  - Cross-sectional snapshot from 2019; may not capture temporal dynamics
  - Geospatial coordinates not explicitly provided; requires geocoding for full mapping
  - Some inconsistencies in file column descriptions (e.g., transect file column counts) requiring careful data inspection
- Potential uses
  - GIS-based analysis of spatial variation in yields and their drivers
  - Visualization of management intensity, BMP adoption, soil characteristics, and understorey structure across farms
  - Scenario analyses linking soil health and vegetation structure to oil palm yields
- Access and interoperability
  - Four CSV files with clearly defined schemas; join on plot_id for integrated analyses
  - Data suitable for reproducible GIS workflows and ecological/agricultural impact studies