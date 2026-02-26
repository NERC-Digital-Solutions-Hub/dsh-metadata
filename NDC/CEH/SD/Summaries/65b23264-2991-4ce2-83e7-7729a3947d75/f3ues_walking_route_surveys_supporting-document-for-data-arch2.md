# Biodiversity and environmental conditions along public walking routes in three UK towns (Bedford, Luton and Milton Keynes), 2014

- Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project aligned with the Biodiversity and Ecosystem Service Sustainability (BESS) programme.
- Aim: document biodiversity and environmental stressors along urban walking routes using standardized tile-based data to enable temporal comparisons and policy scrutiny.

## Study area and design

- Locations: Bedford, Luton, Milton Keynes in southern England.
- Urban form: towns with similar climate/topography; 112 survey tiles (500 m x 500 m) randomly stratified by 25 urban forms using LiDAR and OS MasterMap data.
- Tile selection: five tiles per urban form, non-adjacent, excluding tiles with unusual features; three tiles excluded due to access; final dataset includes tiles with complete route data.
- Data structure: results presented as tile-level syntheses (500 m x 500 m).

## Data collection and components

- Transect routes
  - 700 m walking transects per tile; eight segment lengths (L2–L8) with varying lengths due to access/terrain.
  - Some tiles removed due to incomplete routes or access issues.
- Biodiversity surveys
  - Butterflies: standard Pollard Walk method along transects; survey window 27 Jun–7 Aug 2014, weather suitable; native species list (Table 3) and tile-level richness/abundance.
  - Trees: eight fixed survey points along routes (100 m apart); within 10 m radius, all trees >2 m tall identified to species and native/exotic status (Table 4); native tree richness/abundance used as predictors.
  - Birds: four publicly accessible points per tile; two 10-minute counts (May and June 2014) within 60 m radius; maximum abundance per species across the two surveys used; tile-level species richness and abundance (Table 5).
- Environmental condition surveys
  - Noise: 60-second LAeq measurements at ten points (including route endpoints); mean per tile derived.
  - Temperature: median of two Thermochron loggers per point; field temps compared against Wolfson weather station to compute temperature anomaly (ta_standardised_mean) and tile-level average.
  - Particulate matter: continuous PM readings (PM_small >0.5 µm; PM_large >2.5 µm) along transects (one reading per minute); mean values per tile; PM data missing for eight tiles.
- Landscape and built environment metrics
  - Built cover: road density (all roads and large roads) from OS ITN; distance from urban edge from CIR aerial photography (Landmap) and urban extent; percentage impervious surface (NDVI-based classification with OS MasterMap data); industrial land-use share from multi-source land-use dataset (OS, OSM, AddressBase, MasterMap).
  - Greenspace: foliage height diversity (FHD) derived from LiDAR to 1.5 m resolution with a 1.5 m cell; median greenspace FHD per tile; greenspace patch size (median) and residential garden cover.
  - Socioeconomic: Index of Multiple Deprivation (IMD 2012–13) at tile level (largest IMD proportion within the tile).
- Temporal alignment
  - Environmental data collected on weekdays to reduce day-of-week effects; temperature anomaly uses the nearest weather station as baseline.

## Data structure and variables

- Primary dataset: File 1 – F3UES_walking-routes_all-data.csv
  - Core variables cover:
    - Biodiversity: tree_richness, tree_abundance, native_tree_richness, native_tree_abundance, butterfly_species_richness, butterfly_abundance, bird_species_richness, bird_abundance, etc.
    - Environment: ta_standardised_mean, laeq_mean, pm_small_mean, pm_large_mean, etc.
    - Temporal and spatial descriptors: butterfly_day_of_season, ta_day_of_season, laeq_day_of_season, pm_day_of_season, x_coord/y_coord, transect_id.
    - Landscape and built metrics: pct_grey_cover, median_fhd, urban_boundary_distance, imd_majority_decile, pct_garden_cover, median_patch_size, large_roads_density, all_roads_density, tree_shannon_diversity_index, pct_industrial_cover, etc.
  - Notes: missing data indicated by blanks; some fields derived from supporting documents described below.

- Supporting data files (shapefiles)
  - File set 1: F3UES_walking-routes – transect routes per tile with segmented lengths and start/end points.
  - File set 2: F3UES_walking-routes-points – ten recording points per tile (eight route points plus two environmental points) with coordinates.
  - File set 3: F3UES_urban-edge – urban edge geometry for each town.

- Other related data
  - Bird full point-count dataset deposited separately (NERC EIDC).
  - Land cover map details and LiDAR data processing references provided for replication and methodological transparency.

## Quality, limitations, and data accessibility

- Data limitations
  - PM data missing for eight tiles; tiles with incomplete PM data excluded from PM analyses.
  - LiDAR data missing for 13 tiles; FHD analyses excluded those tiles.
  - Bird analyses excluded 11 tiles due to fewer than four survey points or other access issues.
  - Route variations and access-related length changes noted; some L2–L8 lengths shortened due to access.
- Data quality approach
  - Standardized survey methods across tiles; random stratification by urban form to ensure representative sampling.
  - Clear documentation of data gaps and reasons for exclusions to preserve reproducibility and enable meta-analysis.

- Data usage and related outputs
  - Core analysis and interpretation described in Norton et al. (in press, 2023) with open data references.
  - Bird data and LiDAR-derived metrics archived in dedicated data centers to support reuse and longitudinal studies.

## Purpose and potential applications

- Provides a consistent, tile-based dataset to monitor biodiversity and environmental stressors along urban walking routes.
- Enables assessment of environmental health and policy performance over time and across urban forms.
- Supports analyses of how built environment, greenspace, and socio-economic factors relate to biodiversity and environmental conditions in urban settings.
- Serves as a reproducible framework for urban biodiversity monitoring and for informing urban planning and nature-based solutions.