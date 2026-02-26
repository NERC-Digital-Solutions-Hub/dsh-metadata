# Biodiversity and environmental conditions along public walking routes in three UK towns (Bedford, Luton and Milton Keynes), 2014

## Overview and aims
- A field-based study within the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project to assess biodiversity and environmental conditions along public walking routes.
- Aimed at informing monitoring frameworks: identifying environmental health measures to scrutinise policy, evaluate policy decisions, and inform future decisions.
- Collaboration across multiple UK universities and the British Trust for Ornithology to collect and integrate biodiversity, environmental, and landscape data.

## Study area and design
- Location: three southern English towns with similar climate/topography: Milton Keynes, Bedford, and Luton.
- Tile-based sampling: the combined urban area overlaid with a 500 m x 500 m grid; 112 tiles randomly stratified by urban form were surveyed (five tiles per urban form category, with some exceptions due to access or data gaps).
- Tile classification used LiDAR and OS MasterMap data to define five building-cover and five vegetation-cover categories; tiles were non-adjacent to reduce spatial autocorrelation.
- Survey routes: public walking transects of approximately 700 m within each tile (some tiles excluded due to access).

## Data collection and components
- Butterfly surveys
  - Conducted on-foot along transects using the UK BMS Pollard Walk method during peak butterfly activity (late June–early August 2014).
  - Native butterfly species recorded; tile-level species richness and abundance derived.
- Tree surveys
  - Eight fixed survey points per tile (100 m spacing) plus trees near transects recorded within 10 m of each point and along the route.
  - Species identified to native/exotic status; native tree richness and abundance calculated; tree diversity used as a predictor variable.
- Bird surveys
  - Four publicly accessible survey points per tile; two 10-minute bird counts (May and June 2014) within 60 m radius.
  - Data aggregated to tile-level indices of total bird abundance and species richness; maximum abundance across two surveys used for some analyses.
- Environmental condition surveys
  - Backpack-mounted sensors: noise (LAeq, 60 s, at 10 points per tile), temperature (thermometer loggers), and particulate matter (PM) counters (one reading per minute along transects).
  - Weather comparisons: field temperatures modelled as anomalies relative to the nearest weather station (Wolfson station, Cranfield University); tile-level mean temperature anomaly used as a predictor in models.
- Additional environmental and landscape metrics
  - Built cover: road density (all roads and large roads), distance to urban edge, impervious surface cover, and industrial land-use share.
  - Greenspace: foliage height diversity (FHD) from LiDAR-derived canopy data, median greenspace patch size, and residential garden cover.
  - Urban form and deprivation: IMD (Index of Multiple Deprivation) decile for tiles; distance to urban edge; proportion of gardens.
  - Land-use and greenspace context: percent industrial cover, proportion of greenspace, and greenness metrics derived from Landmap/OS MasterMap and NDVI-based classifications.
- Data integration
  - Landscape-scale remotely sensed data complemented on-the-ground surveys to contextualize biodiversity and environmental conditions.

## Data structure and variables
- Single primary data CSV: F3UES_walking-routes_all-data.csv
  - Key data categories included:
    - Biodiversity: butterfly_species_richness, butterfly_abundance; bird_species_richness, bird_abundance; native_tree_species_richness, native_tree_abundance; total_tree_species_richness, total_tree_abundance.
    - Environmental conditions: ta_standardised_mean (temperature anomaly), butterfly ta (median temperature), laeq_mean (noise), pm_small_mean and pm_large_mean (particulate matter).
    - Temporal and spatial context: butterfly_day_of_season, laeq_day_of_season, pm_day_of_season; ta_day_of_season; point-level timestamps (hour_of_day).
    - Greenspace and built environment: median_fhd, pct_garden_cover, urban_boundary_distance, imd_majority_decile, large_roads_density, all_roads_density, pct_industrial_cover.
    - Site coordinates: x_coord, y_coord (OSGB grid) for tile centroids and routing points.
    - Derived indices: tree_shannon_diversity_index.
  - Data quality: missing values indicated; some tiles had incomplete data due to access or sensor failure; LiDAR-derived data missing for 13 tiles.
- Supporting spatial data
  - File set 1: F3UES_walking-routes (tile-level shapefile of transects with 100 m segments).
  - File set 2: F3UES_walking-routes-points (the ten recording points per tile).
  - File set 3: F3UES_urban-edge (urban edge shapefiles for Milton Keynes, Bedford, and Luton).

## Supporting data and open data context
- Additional data underpinning analyses:
  - Bird point-count data deposited with NERC EIDC.
  - Full land cover map and LiDAR-derived data described and archived (CEDA/NERC).
  - LiDAR processing method and voxel-based canopy metrics documented; open-source tools available.
- Related publications:
  - Norton et al. (in press) Urban Forestry and Urban Greening and associated analyses discussing biodiversity and environmental stressors along urban walking routes.
- Data accessibility and governance:
  - Data and supporting materials are linked to established open-data repositories and project outputs.
  - Data governance and data management practices are described, including sharing of underlying data and metadata, and the need to publicize data provenance and transformations.

## Data quality, challenges, and limitations
- Common monitoring-framing challenges reflected in the study:
  - Data gaps and missing data, especially for particulate matter and LiDAR-derived metrics.
  - Access constraints leading to incomplete routes or tile exclusion.
  - Silo effects and cross-institution collaboration challenges addressed by unified data collection protocols.
  - Metadata completeness: some metadata gaps noted; metadata added to datasets as part of the process to enable verification.
- Temporal scope:
  - Data are from 2014 and reflect a cross-section of urban forms; not a continuous, up-to-date time series.
- Data standardization and transformation:
  - Multiple data streams (biodiversity, environment, land cover) required careful standardization and alignment to tile-level units for integration and modelling.

## Relevance to monitoring-framework authors
- Demonstrates a comprehensive, multi-epoch, multi-source monitoring design integrating biodiversity with environmental stressors and urban form metrics.
- Provides a clear template for data governance, metadata provision, and data sharing across organisations, including:
  - Centralized data file structure with explicit variable definitions.
  - Public data sharing considerations and barriers (e.g., permissions, privacy around private land access).
  - Documentation of data provenance, processing steps, and links to related datasets (LiDAR, land cover, IMD).
- Highlights practical data-quality issues and strategies to mitigate: addressing missing data, documenting access constraints, and reporting data limitations alongside analyses.
- Links data collection to policy-relevant indicators (species richness/abundance, environmental stressors, greenspace metrics, urban form) to inform decision-making and future monitoring efforts.