# Biodiversity and environmental conditions along public walking routes in three UK towns (Bedford, Luton and Milton Keynes), 2014

## Aim
- Document and provide dataset detailing biodiversity and environmental conditions along public walking routes in three southern English towns, enabling exploration of relationships between urban form, greenspace, and ecosystem services.

## Study design and scope
- Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project.
- Field surveys conducted on foot to assess biodiversity and environmental conditions, complemented by landscape-scale remotely sensed data.
- Data presented as 500 m x 500 m tiles (survey tiles) across the combined urban areas of Bedford, Luton, and Milton Keynes.
- Random stratification by urban form used to select survey tiles; 112 tiles initially, with some excluded due to access or incomplete data.

## Study area
- Three towns with similar topography and climate: Milton Keynes (new town grid, greenspace layout), Luton (historic industrial inner town, terraced housing), Bedford (medieval town with radial road network).
- Tile grid overlaid with LiDAR and OS MasterMap data to classify building and vegetation cover.

## Data collection and methods (domains)
- Survey routes
  - 700 m transects per tile along publicly accessible walking routes.
  - Some routes shortened due to access or terrain; incomplete routes excluded from analyses.
- Butterfly surveys
  - Pollard Walk method; one visit between 27 June and 7 August 2014.
  - Data collected on butterfly species richness and abundance per tile.
- Tree surveys
  - Eight fixed survey points along each transect (100 m spacing).
  - Trees within 10 m of points identified to species; native vs non-native classifications per Table 4.
  - Tree richness and abundance computed per tile; native metrics used in specific analyses.
- Bird surveys
  - Four publicly accessible points per tile; two 10-minute counts (May and June 2014) within 60 m radius.
  - Abundance and species richness per tile; uses maximum abundance across two surveys for species-level analyses.
- Environmental condition surveys
  - Noise: 60-second LAeq measurements at ten points (points plus two extra environmental points), with weekly timing aligned to butterfly surveys.
  - Temperature: two Thermochron loggers at each point; field temperature anomaly calculated relative to a nearby weather station (Wolfson, Cranfield University) and averaged by tile.
  - Particulate matter: one-minute readings for small and large particles along entire transect; mean per tile.
  - Weather data: nearest station (Wolfson) used for temperature anomaly calculations; occasionally used as predictor in models.
- Built cover and land-use metrics
  - Road density: all roads and large roads (Dual Carriageways, Collapsed Dual Carriageways, Slip Roads) from OS ITN.
  - Distance to urban edge: centroid-to-edge distance using high-resolution aerial imagery.
  - Impervious surface cover: NDVI-based land-cover map combined with OS MasterMap data.
  - Industrial land-use: classified via OpenStreetMap, AddressBase Plus, and OS MasterMap; 54% built use, 20% green, 3% transport, etc.
- Greenspace metrics
  - Foliage Height Diversity (FHD): derived from full-waveform LiDAR (1.5 m grid; 25 cm vertical resolution); Shannon index calculated per tile for green areas.
  - Median greenspace patch size: based on land-cover patches (Fragstats 4.2).
  - Residential gardens: percent cover from the Mixed Surfaces category in OS MasterMap Topography.
- Socio-economic context
  - Index of Multiple Deprivation (IMD) decile assigned to each tile based on the LSOA that covers the tile.

## Data structure and variables
- Data are provided in one CSV file: F3UES_walking-routes_all-data.csv.
- Key tile-level and route-level variables cover:
  - Biodiversity: butterfly_species_richness, butterfly_abundance, bird_species_richness, bird_abundance, tree_shannon_diversity_index, native_tree_richness, native_tree_abundance, tree_species_richness, tree_abundance.
  - Environment: ta_standardised_mean (temperature anomaly), butterfly_median_ta (median butterfly-season temperature), laeq_mean (noise), pm_small_mean (small particulates), pm_large_mean (large particulates), ta_day_of_season, laeq_day_of_season, pm_day_of_season, ta_hour_of_day, laeq_hour_of_day, pm_hour_of_day.
  - Greenspace: median_fhd, urban_boundary_distance, pct_garden_cover, median_patch_size.
  - Built environment: large_roads_density, all_roads_density, pct_industrial_cover, pct_grey_cover, x_coord, y_coord.
  - Landscape and socioeconomics: imd_majority_decile, imd-related tile identifiers.
- Tile-level metrics are aggregated across the eight fixed survey points and, where appropriate, the transect route.
- Missing data are indicated as blanks; several variables have tile-level or route-level gaps due to access, weather, LiDAR gaps, or incomplete data collection.

## Supporting data and files
- File set 1: F3UES_walking-routes (shapefile) – transect routes per tile with segment lengths and start/end points.
- File set 2: F3UES_walking-routes-points (shapefile) – ten recording points per tile (eight along transect + two environmental points) with coordinates.
- File set 3: F3UES_urban-edge (shapefile) – urban edge geometry for each town.
- Data provenance and methodology details are aligned with Norton et al. (in press, 2023) and related land-cover, LiDAR, and demographic references.

## Data quality, limitations, and notes
- Access-related and terrain-related issues caused some tiles/routes to be excluded or incomplete; 11 tiles excluded from bird analyses due to insufficient point coverage.
- LiDAR-derived FHD data missing for 13 tiles; these tiles were excluded from models using FHD.
- Particulate matter data missing for eight tiles; these tiles were dropped from analyses involving PM.
- Temperature normalization uses a single remote weather station; tile-level temperature anomaly may be influenced by local microclimate not captured by the station.
- Some field variations and route length adjustments are documented (e.g., L7/L8 adjustments, detours for equipment).

## Related data and usage
- The full analysis and interpretation are documented in Norton et al., 2023 (Urban Forestry and Urban Greening, In Press).
- Full bird point-count dataset is deposited with the NERC Environmental Information Data Centre (EIDC).
- Land-cover maps and LiDAR data have dedicated references and open-source processing tools (e.g., voxelate).

## How this data can be used (Data Support perspective)
- Build tile-level dashboards or self-serve reports to explore relationships between biodiversity, environmental stressors, urban form, greenspace structure, and socio-economic context.
- Integrate with other municipal datasets (e.g., planning, air quality) to assess urban planning scenarios and biodiversity outcomes.
- Use the standardized 500 m x 500 m tile framework to compare across towns or replicate in other urban areas.
- Leverage the shapefiles and derived metrics (road density, urban edge distance, FHD, patch size, garden cover) for spatial modeling and landscape-scale analyses.
- Utilize the CSV file as a core data source for regression or machine-learning models predicting biodiversity indicators from environmental and built-form predictors.