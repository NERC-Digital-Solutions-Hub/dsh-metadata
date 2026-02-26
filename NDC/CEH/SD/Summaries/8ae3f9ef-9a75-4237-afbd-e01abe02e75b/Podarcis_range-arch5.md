# Supporting information for modelling the extent of spatial spread and population growth in introduced populations of a non-native lizard ( Podarcis muralis ) in England

## Executive overview of data assets
- Datasets comprise presence data and background points with associated environmental data for MaxEnt modelling of Podarcis muralis.
- UK-specific presence inputs: uk_pods.csv; native range inputs: native_pods.csv; all records combined: all_pods.csv.
- Local and regional Raster inputs: .asc files containing raw spatial parameters (e.g., distance to nearest road) used for local modelling; outputs from local MaxEnt models include .txt files used as landscape layer inputs for RangeShifter.
- RangeShifter outputs: projected population growth per landscape cell and x/y coordinates, provided in Pop.csv and avg.csv (averaged over 50 replicates).
- Local site data: files with suffix _pods.csv give point locations (x, y in OSGB 1936 / British National Grid) for UK sites and specific localities (e.g., east_pods.csv, port_pods.csv, abbot_pods.csv, etc.).
- Background and presence data schema: local_background_points.csv and local_podarcis_presence.csv describe variables such as NDVI, habitat phase, insolation, and proximity to roads/rail/buildings with coordinates.
- RangeShifter site files: individual site prefixes (e.g., bourne, east, port, abbot, etc.) with _max_15.txt (MaxEnt output), _cost_15.txt (local movement cost surface), and _release.txt (initial release locations).
- Output files: <SITE>_pop.csv and <SITE>_avg.csv summarize simulation results across 50 replicates (per year, per cell, and demographic breakdowns).
- Raster and map inputs: study-area specific .asc files named as <STUDY_AREA>_<VARIABLE>.asc, covering components like _ndvi, _phase, _spring, _road, _rail, _build.
- All data are described with additional context in Tables 1–4 and Figure 2 in the document.

## Data collection, provenance, and sampling
- Field sightings collected across three field seasons (April–September) in 2016–2018: 1331 lizard sightings across 25 sites.
- Data sources: online portal (76 credible sightings), postcard returns (52 confirmed sightings), and visual surveys.
- Lead personnel for data collation and interpretation: R. Williams and L. Mendes da Costa.
- Visual surveys: conducted 07:30–18:00 under suitable sun, GPS-recorded locations to ±1 m, overlay of GPS data on aerial images for precision.
- Railway transect study at West Worthing, Sussex: ~9.5 km transect with 21 survey points and 11 artificial refugia; access constraints led to uneven sampling; refugia left in place briefly due to time limits.
- Community engagement: door-to-door canvassing in 2017–2018 (500 postcards sent; 76 credible records; 114 online portal users); Participatory GIS (PPGIS) via map-me.org captured sightings with metadata questions to assess veracity; some sightings ground-truthed.
- Media outreach: 2017 local press release to raise awareness and invite sightings.
- Data validation: sightings near known populations validated via site visits and aerial overlays; records extending known extents were ground-truthed.

## Data quality, limitations, and governance considerations
- Sampling design considerations: data thinning (10 km) applied to reduce spatial autocorrelation; UK presence data reduced to 25 records; native range data (from GBIF) to 1542 records.
- Validation processes for citizen science data: location accuracy, photographic evidence (where provided), proximity to known populations, and structured responses to targeted questions; questionable records were rejected or subject to site verification.
- Limitations and biases: uneven survey effort across sites; access constraints (railway vs public land) affecting data completeness; potential biases inherent in crowdsourced data and variable detection probabilities.
- Data availability and sharing: multiple data streams (field surveys, PPGIS, portal sightings, media reports) with some records requiring validation before inclusion in modelling datasets; data are prepared for sharing via SWD and online portals with explicit provenance.
- Update and governance: datasets are structured for ongoing updates, with explicit naming conventions and documentation to support versioning and reproducibility; cross-referencing of input (presence) and background data with modeling outputs.

## Modelling inputs, methods, and data products
- Climate and habitat modelling framework:
  - MaxEnt v3.3.3k used to develop relative habitat suitability maps at national (UK) extent.
  - Data thinning to minimize spatial autocorrelation performed with SpThin; 25 UK records and 1542 native records used for comparisons across three model setups: UK presence only, native range only, and combined UK + native data.
  - Ten climatic variables drawn from WorldClim and ENSEMBLES (E-OBS) used after reducing covariation; resolution harmonized (0.0083° for WorldClim, 0.25° for E-OBS; interpolation applied).
  - Model complexity controlled by linear features only and a regularization multiplier of 2; other settings kept default.
  - Local habitat modelling uses 1083 presence records across 10 study locations; 2 m resolution environmental variables for MaxEnt inputs; six variables included in local models (NDVI, distance to buildings/roads/rail, spring insolation, etc.).
- Local-range expansion modelling (RangeShifter IBM):
  - Spatially explicit individual-based models (RangeShifter v1.1) translate MaxEnt outputs into habitat quality (1–100) and a movement cost surface (1–10) after rescaling habitat suitability.
  - Inputs resampled to 15 m × 15 m cells to balance memory use with ecological relevance; initial population distribution set from known introduction sites or population centers.
  - Demography and behaviour parameterised from literature (Table 2), with calibration to replicate observed extents; default values used where direct data unavailable.
  - Simulations run for the introduced period up to 2040 with 50 replicates per site; local extinction probability set at 0.003 per year to introduce stochasticity.
- Data file structure and nomenclature (examples):
  - Pod data by site and region stored as uk_pods.csv, native_pods.csv, all_pods.csv; local site data such as east_pods.csv, port_pods.csv, etc.
  - Background/presence data files: local_background_points.csv and local_podarcis_presence.csv contain per-point attributes and OSGB coordinates (x, y).
  - RangeShifter outputs per site: <SITE>_pop.csv and <SITE>_avg.csv; model inputs/outputs include <SITE>_max_15.txt (MaxEnt input), <SITE>_cost_15.txt (cost layer), and <SITE>_release.txt (release location).
  - Local study-area rasters are named as <STUDY_AREA>_<VARIABLE>.asc, covering 9 areas and variables listed (e.g., bourne_phase.asc, port_road.asc).
- Data sources and references: climate data (WorldClim, E-OBS), GBIF for native-range records, Landsat-derived NDVI, OS Open Map for distance calculations, LIDAR-based elevation data, and multiple literature sources for demographic parameters (Table 2 references).

## Coordinate systems, resolutions, and data formats
- Geographic coordinates and data are provided in OSGB 1936 / British National Grid; point data use x, y coordinates accordingly.
- Local-scale inputs at 2 m resolution (NDVI, distance to features, insolation) and 15 m × 15 m for RangeShifter movement/carrying capacity layers.
- Raster and ASCII files (.asc) cover region-specific variables with explicit naming conventions and study-area mappings.
- Output data tables (.csv) and simulation results (.txt, .csv) follow site-specific prefixes to enable traceability of results.

## Access, reuse, and metadata implications for Data Stewards
- Data are accompanied by extensive metadata within the document (Tables 1–4) and are linked to commonly used modelling tools (MaxEnt, RangeShifter) with explicit parameter settings to enable reproducibility.
- PPGIS and field data are integrated with traditional survey data, with validation steps described to ensure data quality before inclusion in models.
- Data formats are interoperable (CSV, TXT, ASC) and coordinate systems standardized to OSGB for spatial analyses, supporting cross-system data workflows.
- Sharing and reuse considerations include transparency about data sources (WorldClim, ENSEMBLES, GBIF, OS VectorMap Local, Landsat, etc.) and clear documentation of site-specific data (UK and local profiles) to facilitate reuse in similar niche-modelling contexts.
- Acknowledgement of data challenges such as incomplete user-needs capture, variable data quality from citizen science inputs, access constraints, and potential biases, underlines the importance of ongoing data governance, provenance tracking, and versioned updates.

## Governance and data stewardship takeaways
- Maintain thorough metadata and versioning for all inputs and outputs, with explicit linkage between input datasets (presence, background, environmental variables) and modelling results (MaxEnt outputs, RangeShifter inputs/outputs).
- Ensure consistent data quality checks, provenance, and validation procedures for citizen-science-derived data (PPGIS and postcard responses) alongside formal survey data.
- Document coordinate systems, resolutions, and file naming conventions to support interoperability across systems and future updates.
- Plan for updates to datasets with new field seasons or additional sightings, maintaining traceability from raw data to modelling outputs and ensuring appropriate access controls and licensing where applicable.