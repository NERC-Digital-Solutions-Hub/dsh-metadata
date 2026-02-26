# Biodiversity and environmental conditions along public walking routes in three UK towns (Bedford, Luton and Milton Keynes), 2014

- Overview
  - A comprehensive data collection as part of the F3UES project to assess biodiversity and environmental conditions along public walking routes in Bedford, Luton, and Milton Keynes, UK (2014).
  - Integrates field surveys (butterflies, birds, trees) with environmental measurements (noise, temperature, particulate matter) and landscape context (land cover, greenspace metrics, built environment metrics) derived from remote sensing and secondary data.
  - Data are organized at the 500 m x 500 m tile level, enabling tile-scale analyses across a spectrum of urban forms.

- Study and organizational context
  - Institutions: University of Sheffield, British Trust for Ornithology (BTO), University of Exeter, Cranfield University; contributions span urban form assessment, route selection, biodiversity surveys, and GIS/land-cover data creation.
  - Related publications: Norton et al. (in press) describing methods and analyses; data used to support findings in Urban Forestry and Urban Greening (2023, in press).

- Data scope and structure
  - Study area: Three southern England towns with similar climate/topography; data collected across 112 survey tiles (500 m x 500 m each); some tiles excluded due to access issues or incomplete data.
  - Data file: One primary CSV (F3UES_walking-routes_all-data.csv) containing biodiversity surveys, environment condition surveys, and landscape land-use/land-cover measures.
  - Supporting spatial data: Three shapefiles detailing walking routes, stopping points, and urban edges (File sets 1–3).
  - Additional related data: Full bird point-count data (NERC EIDC deposit), full land-cover map, LiDAR-derived greenspace metrics (FHD), and LiDAR data archived in CEDA.

- Study design and sampling
  - Tile selection: 500 m x 500 m grid over combined urban areas; random stratification to capture diverse urban forms based on building and vegetation cover derived from LiDAR and OS MasterMap data.
  - Urban form categorization: 25 forms (five building-cover classes x five vegetation-cover classes). Five tiles per form attempted, with constraints (no adjacency, no unusual features); reduces to 112 tiles (plus exclusions).
  - Transect routes: Public walking routes within each tile; total nominal transect length is 700 m (with adjustments for access and terrain). Some tiles excluded due to access issues or incomplete routes.

- Data collection methods
  - Butterfly surveys
    - Pollard Walk method; 27 June–7 August 2014; one daily visit (10 am–5 pm) with a 5 m survey cube ahead of the observer.
    - Native species only; tile-level species richness and abundance calculated.
  - Tree surveys
    - Eight fixed survey points per tile (100 m apart) within 10 m radius; native and exotic species identified; center-trunk trees within transects also recorded.
    - Outputs include native tree species richness, native tree abundance, and a tree diversity index.
  - Bird surveys
    - Four publicly accessible points per tile; two 10-minute counts (May and June 2014); 60 m radius; analysis uses maximum abundance across the two surveys to estimate true abundance and tile-level species richness.
  - Environmental condition surveys
    - Backpack-mounted sensors recorded: noise (LAeq, dBA) for 60 seconds at each point; temperature via two Thermochron ibuttons; data collected on weekdays to reduce day-of-week effects.
    - Weather data: Temperature anomaly relative to the Wolfson Weather Station (Cranfield) used as a predictor in models.
    - Particulate matter: PM readings (>0.5 µm and >2.5 µm) collected continuously along the transect (one reading per minute) with a Dylos DC1700.
  - Greenspace and built-environment metrics
    - Built cover: road density and distance-to-edge metrics derived from OS MasterMap ITN data and CIR imagery.
    - Greenspace metrics: foliage height diversity (FHD) from LiDAR (1.5 m resolution voxel map; Shannon index), median greenspace patch size, residential garden cover.
    - Additional metrics: Industrial land-use share, impervious surface cover, distance from urban edge, and Index of Multiple Deprivation (IMD) at tile level.

- Data structure and variables
  - Core data file: F3UES_walking-routes_all-data.csv
  - Key variable groups (examples)
    - Transect and biodiversity: transect_id, butterfly_species_richness, butterfly_abundance, bird_species_richness, bird_abundance, tree_species_richness, native_tree_species_richness, native_tree_abundance, tree_shannon_diversity_index.
    - Environmental conditions: butterfly_median_ta, ta_standardised_mean (temperature anomaly), laeq_mean (noise), pm_small_mean, pm_large_mean, ta_hour_of_day, laeq_hour_of_day, pm_hour_of_day.
    - Landscape context: pct_grey_cover (impervious/urban cover), median_fhd (foliage height diversity), urban_boundary_distance, imd_majority_decile, pct_garden_cover, median_patch_size, large_roads_density, all_roads_density, x_coord/y_coord (tile centroids in British National Grid).
    - Data completeness: Missing data indicated as blanks; reasons discussed in the text (e.g., access issues, data gaps).
  - Supporting files provide spatial context and route details:
    - F3UES_walking-routes: route geometry by tile and 100 m segments.
    - F3UES_walking-routes-points: stop points along routes and coordinates.
    - F3UES_urban-edge: urban boundary edges for each town.
  - Additional data domains referenced: bird point-count data, land-cover map, LiDAR-derived FHD data.

- Data quality, completeness, and limitations
  - Exclusions and gaps
    - 3 tiles excluded due to access issues; routes not completed to 700 m.
    - 11 tiles excluded from bird analyses due to fewer than four survey points.
    - Particulate matter readings missing for eight tiles; LiDAR data missing for 13 tiles (affecting FHD-based greenspace metrics).
  - Data handling
    - Some route segment lengths vary due to access and terrain; notes provided on specific variations.
    - Temperature data alignment uses a weather-station-based anomaly, with tile-level aggregation.
  - Documentation and provenance
    - Methods and variables are aligned with Norton et al. (in press); full methodological description is provided and cross-referenced.
    - Additional related datasets and data citations provided (NERC EIDC deposit, Landmap imagery, LiDAR data in CEDA).

- Intended reuse and governance
  - Purpose: To enable analyses of biodiversity and environmental stressors in urban walking-route contexts and to support urban ecosystem service research.
  - Data custody and sharing
    - Primary data are provided in CSV with rich metadata and linked shapefiles for spatial context.
    - Related data (bird point counts, land-cover maps, LiDAR datasets) are archived in appropriate data repositories (EIDC, CEDA).
  - Documentation and usage notes
    - Clear descriptions of measurement methods, units, and data structure are included to facilitate reproducibility and integration with other datasets.
    - Background and rationale are documented in Norton et al. (in press) and supplementary references.

- How this dataset can support governance and data stewardship
  - Provides a well-documented, tile-based, multi-taxa biodiversity and environmental dataset for urban form analyses, suitable for governance-focused data cataloging, metadata standardization, and interoperability with other urban environmental datasets.
  - Includes multiple data modalities (tabular biodiversity/ENV metrics and extensive GIS-derived landscape metrics) enabling cross-domain analyses while highlighting data gaps and exclusions for responsible data use.
  - Clear provenance, file structure, and external data references support discoverability, traceability, and data-sharing compliance across organisations.