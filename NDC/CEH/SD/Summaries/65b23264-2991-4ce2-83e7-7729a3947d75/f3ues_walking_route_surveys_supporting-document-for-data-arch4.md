# Biodiversity and environmental conditions along public walking routes in three UK towns (Bedford, Luton and Milton Keynes), 2014

- Overview
  - A multi-institution field study (2014) assessing biodiversity and environmental conditions along public walking routes in Bedford, Luton, and Milton Keynes, complemented by landscape-scale remote sensing data.
  - Purpose: provide tile-based, survey-level data to support analyses of urban biodiversity and environmental stressors; part of the F3UES project within the BESS programme.
  - Collaborating organisations: University of Sheffield, British Trust for Ornithology (BTO), University of Exeter, Cranfield University; with roles in site selection, route surveying, data collection, and GIS/land-cover processing.

- Data scope and structure
  - Study units: 112 randomly selected 500 m x 500 m tiles (tiles were not directly adjacent; some tiles excluded due to access issues).
  - Transects: publicly accessible walking routes of ~700 m per tile (some variation due to access/terrain); data are provided as tile-level syntheses (File set 1) and route-point data (File sets 2 and 3).
  - Primary data file: F3UES_walking-routes_all-data.csv, containing biodiversity surveys, environmental conditions, and landscape/built-environment metrics for each tile.
  - Supporting spatial data: three shapefiles (F3UES_walking-routes, F3UES_walking-routes-points, F3UES_urban-edge) detailing routes, stopping points, and urban-edge geometry.

- Biodiversity data
  - Butterflies: presence and abundance recorded along each transect using the Pollard Walk method; 15 butterfly species observed (list includes common species such as Small Tortoiseshell, Meadow Brown, Painted Lady, Common Blue, etc.); tile-level butterfly species richness and abundance calculated.
  - Birds: point-count data collected at four publicly accessible points per tile in May and June 2014; two 10-minute counts per point; tile-level indices for total bird abundance and species richness; data primarily native birds with a subset of non-natives noted.
  - Trees: eight fixed survey points per tile (within 100 m spacing along transects) and additional trees crossing the transect; species identified to native/exotic status; both total and native tree richness/abundance calculated; trees within 10 m of survey points used for tree diversity index (used as a predictor in models).

- Environmental condition data
  - Noise: 60-second LAeq measurements at ten survey points per tile; mean per point and tile averages calculated (dBA).
  - Temperature: field measurements at survey points; anomalies calculated relative to the Wolfson weather station (Cranfield University) and averaged at tile level; use of the Wolfson station temperature as a baseline in modelling.
  - Particulate matter: PM measurements (small >0.5 µm and large >2.5 µm) recorded at one-minute intervals along transects; mean values computed per tile; PM data missing for eight tiles and excluded from analyses.

- Greenspace and built-environment metrics
  - Greenspace structure: foliage height diversity (FHD) derived from full-waveform LiDAR (1.5 m grid with 25 cm vertical resolution; Shannon index applied to canopy voxels); median FHD computed for green areas per tile.
  - Greenspace size: median greenspace patch size calculated from land-cover data.
  - Residential gardens: percent garden cover derived from OS MasterMap “Mixed Surfaces” category.
  - Built-cover measures: road density (all roads and large roads defined by OS ITN categories), distance from urban edge (centroid to urban-edge edge using CIR imagery), and percentage impervious surface cover (NDVI-based classified land-cover with OS MasterMap integration).
  - Industrial land use: share of tile area classified as industrial land, compiled from OpenStreetMap, AddressBase Plus, and OS MasterMap data.

- Socioeconomic context
  - Index of Multiple Deprivation (IMD) decile used as a tile-level contextual variable, selecting the decile covering the majority of each tile.

- Data quality, limitations, and exclusions
  - Access- and terrain-related exclusions: some tiles could not be surveyed to the full 700 m, and 11 tiles were excluded from bird analyses due to insufficient point coverage or unsuitable habitat.
  - Missing data: particulate matter data missing for eight tiles; LiDAR data missing for 13 tiles; incomplete tile data led to exclusions in respective analyses.
  - Temporal scope: data pertain to 2014; environmental and biodiversity measures reflect conditions during the 2014 survey window (June–August for butterflies; May–June for birds).
  - Variability considerations: route length variations and necessary in-field adjustments noted; some back-pack instrumentation detours described in procedural notes.

- Data provenance and related resources
  - Methods and background rationale described in Norton et al. (in press, 2023) and linked supplementary documents; the dataset aligns with the open data and landscape-ecology-derived measures described in Grafius et al. (2016, 2018) and Hancock et al. (2017).
  - Full bird count dataset deposited with the NERC Environmental Information Data Centre (EIDC) under Plummer & Siriwardena (2023).
  - LiDAR-derived FHD and land-cover metrics built from multiple data sources (OS MasterMap, OpenStreetMap, CIR imagery); LiDAR data processing and voxel-based canopy metrics described in cited literature.

- Access, reuse, and governance
  - Data presented as a single CSV (File 1) with clearly defined variable descriptions and missing-data indicators; accompanying shapefiles (File Set 1–3) provide spatial context for tiles, routes, and urban edges.
  - Data intended to support the Norton et al. analyses on urban biodiversity and environmental stressors, with open avenues for reuse in urban ecology, data-system planning, and cross-sector collaboration.
  - Provenance and data lineage documented, enabling exploration of data aggregation, scale effects, and cross-referencing with land-cover and LiDAR-derived metrics for replication or extended modelling.

- Relevance for data leadership and data-system considerations
  - Demonstrates end-to-end data lifecycle: careful tile stratification, multi-source data fusion (biological surveys, environmental sensors, LiDAR, land-cover, and socioeconomics), and clear data products (tile-level summaries and supporting spatial datasets).
  - Illustrates data discoverability, interoperability, and reuse potential across sectors (academic, government, conservation, urban planning) through standardized tile identifiers and comprehensive metadata.
  - Highlights practical data governance topics for leaders: handling data gaps and exclusions, documenting field-method variations, ensuring metadata clarity, and maintaining links to external data sources (OS MasterMap, OpenStreetMap, LiDAR archives).

- Key references and related outputs
  - Norton BA et al., 2023. Biodiversity and environmental stressors along urban walking routes. Urban Forestry and Urban Greening. (In press; data and methods described here underpin that work.)
  - Supporting data and LiDAR/land-cover references provided for replication and methodological context, along with EIDC deposition for the bird data.