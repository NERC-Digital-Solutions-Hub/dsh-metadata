# Biodiversity and environmental conditions along public walking routes in three UK towns (Bedford, Luton and Milton Keynes), 2014

- A field-based study within the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project assessing biodiversity and environmental conditions along public walking routes.
- Data collected in Bedford, Luton (Luton-Dunstable area) and Milton Keynes (southern England) with landscape-scale remotely sensed data for context.
- Data are tile-based (500 m x 500 m) and intended for analysis of urban form, greenspace, and environmental stressors on biodiversity.

## Study area and sampling design

- Towns: Milton Keynes, Bedford, Luton.
- Grid: overlay of a 500 m x 500 m tile grid across combined urban areas; random stratification across 25 urban-forms using building cover (five classes) and vegetation cover (five classes) to select tiles for surveying.
- Tiles surveyed: 112 tiles (surveyed tiles; some excluded due to access or data gaps).
- Purpose: capture a spectrum of urban forms and environmental conditions; tile-level analyses link biodiversity to urban form and landscape metrics.

## Data collection and survey programs

- Survey routes: publicly accessible walking routes within each tile; transects of about 700 m (with variations due to access/terrain); some tiles excluded if a full route could not be completed.
- Butterfly surveys: standardized Pollard Walk method along transects (June 27 – August 7, 2014); one visit per route; native species only; tile-level butterfly species richness and abundance.
- Tree surveys: fixed points along transects (eight points per route, 100 m apart); identify trees >2 m within 10 m of points; native vs. non-native classification; tile-level native tree species richness and abundance (and overall tree richness/abundance).
- Bird surveys: four publicly accessible points per tile; two 10-minute point counts (May and June 2014) within 60 m radius; abundance and richness per tile; use maximum abundance per species across two surveys to estimate true abundance.
- Environmental condition surveys: temperature and noise measurements using backpacks at the eight fixed points plus two additional ones; particulate matter counts along the entire transect; weather data referenced to a nearby Cranfield Wolfson weather station; weekday sampling to minimize day-of-week effects.

## Spatial and landscape data integrated with field data

- Built cover metrics:
  - Road density: density of all roads and density of large roads (Dual Carriageways, Collapsed Dual Carriageways, Slip Roads) from OS MasterMap ITN.
  - Distance from urban edge: tile centroid to nearest edge of built-up area (from 0.5 m CIR aerials; LandMap).
  - Percent impervious surface cover: derived from land-cover layer using NDVI and OS MasterMap.
  - Industrial land-use share: land-use map combining OpenStreetMap, AddressBase Plus, and MasterMap data; 54% built-use, 20% green-use, etc.
- Greenspace metrics:
  - Foliage Height Diversity (FHD): LiDAR-based 3D canopy metric (1.5 m horizontal x 25 cm vertical voxel map; Shannon diversity per vertical stack).
  - Median greenspace patch size: derived via Fragstats from land-cover classes.
  - Residential gardens: cover percentage from OS MasterMap Topography Mixed Surfaces.
- Proximity and deprivation:
  - Urban edge distance: distance from tile centroid to urban edge.
  - Index of Multiple Deprivation (IMD): 2012-13 decile-based measure applied to tiles by majority LSOA coverage.
- Data sources for full context include LiDAR, land cover maps, road networks, and historical aerials (Landmap).

## Data structure and variables

- File 1: F3UES_walking-routes_all-data.csv
  - transect_id: tile identifier (500 m x 500 m).
  - tree_species_richness, tree_abundance: total trees and species richness across eight survey points.
  - native_tree_species_richness, native_tree_abundance: native trees only.
  - butterfly_species_richness, butterfly_abundance: butterfly metrics along transects.
  - butterfly_day_of_season, butterfly_median_ta, ta_standardised_mean, ta_day_of_season, ta_hour_of_day: butterfly temperature metadata and seasonal timing.
  - laeq_mean, laeq_day_of_season, laeq_hour_of_day: noise (LAeq) metrics at points and tile-level averages.
  - pm_large_mean, pm_small_mean, pm_day_of_season, pm_hour_of_day: particulate matter counts along transects.
  - bird_species_richness, bird_abundance: bird metrics across four survey points; includes native vs non-native; percent grey cover (buildings/paved) and greenspace-derived predictors.
  - median_fhd: median foliage height diversity for greenspaces (from LiDAR).
  - urban_boundary_distance: tile distance to urban edge.
  - imd_majority_decile: IMD decile for the tile.
  - pct_garden_cover: residential garden share.
  - median_patch_size: greenspace patch size.
  - large_roads_density, all_roads_density: road density metrics per tile.
  - tree_shannon_diversity_index: tree diversity across points and route.
  - pct_industrial_cover: industrial land-use share.
  - x_coord, y_coord: tile centroid grid coordinates (British National Grid).
- Supporting spatial data files:
  - File set 1: F3UES_walking-routes (transit lines and segments).
  - File set 2: F3UES_walking-routes-points (survey points and coordinates).
  - File set 3: F3UES_urban-edge (urban edge shapefile per town).
- Data are provided with missing values filled as blanks; reasons for missing data described in text.

## Data quality, limitations, and scope

- Access-related exclusions: 3 tiles excluded due to access; 11 tiles excluded for bird analyses due to incomplete point coverage.
- Missing data:
  - Particulate matter data missing for eight tiles (dropped from analysis).
  - LiDAR data missing for 13 tiles (greenspace FHD analyses dropped for those tiles).
  - Some route segments had length variations due to access or terrain; documented in the dataset notes.
- Temperature data: temperature modeled as anomaly relative to a nearby weather station (Wolfson Cranfield) with tile-level aggregation.
- Data are designed for regression-type analyses linking urban form and environmental stressors to biodiversity measures, as described in Norton et al. (in press, 2023).

## Related information and data accessibility

- Primary analysis reference: Norton BA et al. 2023. Biodiversity and environmental stressors along urban walking routes. Urban Forestry and Urban Greening. In press. Data and methods description align with this work.
- Supporting data deposit: point-count bird data for 2014, deposited with NERC EIDC.
- Land cover and LiDAR data sources and processing are described in Grafius et al. (2016, 2018) and Hancock et al. (2017); open-source tools for LiDAR processing are provided.
- Spatial data and data structure designed for GIS analyses and map-based visualization, suitable for cross-tine urban form and biodiversity studies.