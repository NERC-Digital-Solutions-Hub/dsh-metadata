# Biodiversity and environmental conditions along public walking routes in three UK towns (Bedford, Luton and Milton Keynes), 2014

- Aim and scope
  - Field surveys to assess biodiversity and environmental conditions along public walking routes.
  - Integrated with landscape-scale remotely sensed data to characterise surrounding landscape.
  - Study uses random stratification by urban form across three southern English towns.

- Study area and sampling design
  - Towns: Bedford, Luton, Milton Keynes.
  - Land area overlaid with 500 m x 500 m tiles; 112 survey tiles surveyed ( Tiles were randomly selected to represent five of 25 urban forms; no adjacent tiles; excluded tiles due to access issues).
  - Urban forms categorized by building cover and vegetation cover using LiDAR and OS MasterMap data.

- Data collection overview (types and timing)
  - Butterfly surveys
    - Method: Pollard Walk; one visit per tile between 27 June and 7 August 2014.
    - Standard 5 m cube search area; weather conditions aligned with UKBMS method.
    - Outputs: butterfly species richness and abundance per tile.
  - Bird surveys
    - Sites: four publicly accessible points per tile.
    - Timing: two 10-minute counts in May and June 2014; detectability considerations applied.
    - Outputs: tile-level total bird abundance and species richness; maximum per point used to estimate true abundance.
  - Tree surveys
    - Eight fixed survey points along each transect (100 m spacing); trees >2 m tall within 10 m of points recorded.
    - Species identified; native vs exotic classification (Table 4); native-tree-based metrics calculated.
    - Outputs: tile-level native tree species richness and native tree abundance; overall tree richness and abundance.
  - Environmental condition surveys
    - Backpack-based measurements along transects: noise (LAeq, dBA), temperature (thermometer loggers), and particulate matter (PM) counts (small >0.5 μm and large >2.5 μm).
    - Data collected at the eight fixed points plus two additional environmental points; weekday-only sampling to minimise day-of-week effects.
    - Temperature data linked to a nearby weather station (Wolfson station, Cranfield University) to compute temperature anomaly (tile mean).
  - Particulate matter
    - PM counts recorded continuously at one-minute intervals; means calculated across transects.
    - Data missing for eight tiles and were excluded from analyses for PM-related models.
  - Greenspace and built environment metrics
    - Built cover: road densities (all roads and large roads) from OS MasterMap ITN.
    - Distance to urban edge: from tile centroid to urban edge using CIR imagery and Landmap data.
    - Impervious surface: NDVI-based classification with OS MasterMap overlay.
    - Industrial land use: derived from a composite land-use dataset combining OpenStreetMap, AddressBase Plus, and OS MasterMap.
    - Greenspace structure: foliage height diversity (FHD) from LiDAR-derived 1.5 m resolution voxel map; median FHD across greenspaces.
    - Greenspace size: median patch size using Fragstats-based analysis.
    - Residential gardens: percent garden cover from OS MasterMap Mixed Surfaces category.
    - Socioeconomic context: Index of Multiple Deprivation (IMD) decile (2012-13) mapped to tile areas.
  - Weather and temperature
    - Temperature anomaly (ta_standardised_mean) computed per tile as mean of point anomalies relative to Wolfson station.
    - Butterfly temperature (butterfly_median_ta) and corresponding day/hour metadata captured for temporal alignment.

- Data structure and variables
  - Primary data file: F3UES_walking-routes_all-data.csv
  - Key variable groups
    - Transect and tile identifiers: transect_id
    - Biodiversity: butterfly_species_richness, butterfly_abundance, bird_species_richness, bird_abundance, native_tree_species_richness, native_tree_abundance, tree_species_richness, tree_abundance
    - Temperature and weather: butterfly_day_of_season, butterfly_median_ta, ta_standardised_mean, ta_day_of_season, ta_hour_of_day
    - Noise and environment: laeq_mean, laeq_day_of_season, laeq_hour_of_day
    - Particulate matter: pm_small_mean, pm_large_mean, pm_day_of_season, pm_hour_of_day
    - Greenspace and built environment: median_fhd, urban_boundary_distance, imd_majority_decile, pct_garden_cover, median_patch_size, large_roads_density, all_roads_density, tree_shannon_diversity_index, pct_industrial_cover, pct_grey_cover
    - Spatial coordinates: x_coord, y_coord
  - Data quality notes
    - Missing data indicated by blanks; several tiles excluded due to access, data gaps, or incomplete sampling.
    - Specific exclusions: tiles with insufficient bird counts (11 tiles total) and tiles lacking PM or LiDAR data (PM: 8 tiles missing; LiDAR: 13 tiles missing).

- Supporting data and spatial files
  - File set 1: F3UES_walking-routes (shapefile) – transect route geometry and segment details.
  - File set 2: F3UES_walking-routes-points (shapefile) – stop points along transects for environmental data collection.
  - File set 3: F3UES_urban-edge (shapefile) – urban edge for each town.
  - Additional documentation links and methodological notes available in Norton et al. (in press).

- Data provenance and related work
  - Primary analyses and interpretation described in Norton et al. 2023 (Urban Forestry and Urban Greening, in press).
  - Full bird point-count dataset deposited with NERC EIDC; LiDAR, land cover, and related datasets archived with CEDA/NERC resources.
  - Methods for LiDAR-derived FHD and landscape metrics described in cited literature.

- Limitations and considerations for analysis
  - Data gaps due to access, weather, or coverage issues; tiles with missing PM, LiDAR, or bird point counts excluded from relevant analyses.
  - Tile-level comparisons must account for variable route lengths, access issues, and potential non-stationarity in urban form categories.
  - Temperature anomaly and other environmental predictors derived from proximal weather data and LiDAR-based landscape metrics to ensure comparability across tiles.

- Practical implications for analysts
  - Rich, multi-dimensional dataset enabling correlations between biodiversity (butterflies, birds, trees) and environmental stressors (noise, temperature, PM) across urban forms.
  - A wide array of built and greenspace metrics supports modeling of urban ecosystem services and biodiversity responses to urbanization.
  - Data are organized for tile-level analyses with clearly defined predictors and outcome variables, suitable for correlation, regression, and predictive modeling.