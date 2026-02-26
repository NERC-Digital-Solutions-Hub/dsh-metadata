# Supporting information for modelling the extent of spatial spread and population growth in introduced populations of a non-native lizard ( Podarcis muralis ) in England

## Overview
- Provides data and methods used to model spatial spread and population growth of Podarcis muralis in England.
- Combines MaxEnt habitat suitability modelling (national and local scales) with RangeShifter individual-based modelling (IBM) to project population growth and spread.
- Data sources include UK field surveys, public reports, media outreach, and ecological datasets; 1331 lizard sightings across 25 sites were collected over 2016–2018.
- Outputs include local and national habitat suitability maps, movement costs, release sites, and simulated population counts by landscape cell across 50 replicates up to 2040.

## Data and inputs
- Datasets contain species presence points, background points, and associated environmental data for MaxEnt and RangeShifter inputs.
- Presence data files:
  - uk_pods.csv (UK records)
  - native_pods.csv (native range records)
  - all_pods.csv (UK + native range)
- Local rasters and model inputs:
  - .asc files with parameters (e.g., distance to roads) for local regions
  - Local and national environmental variables at fine resolutions (e.g., NDVI, building/road/rail distance, insolation)
  - SWD (sample with data) inputs for local MaxEnt projections
  - RangeShifter inputs: _max_15.txt (MaxEnt outputs), _cost_15.txt (cost surface), _release.txt (initialisation)
- RangeShifter outputs:
  - <SITE>_pop.csv and <SITE>_avg.csv (population counts per cell across replicates and years)
- Site-level location data:
  - Files named uk_pods.csv, east_pods.csv, port_pods.csv, abbot_pods.csv, bury_pods.csv, ferrer_pods.csv, folk_pods.csv, shore_pods.csv, wemb_pods.csv, worth_pods.csv (OSGB coordinates)
- Local background and presence files:
  - local_background_points.csv
  - local_podarcis_presence.csv
  - Variables include _ndvi, _phase, _spring, _road, _rail, _build, x, y
- Local study areas and variable set:
  - Study-area specific ASC files (bourne, east, port, abbot, bury, ferrer, folk, shore, wemb, worth) with _ndvi, _phase, _spring, _road, _rail, _build
- Documentation and references accompany the data (methods and variable definitions).

## Field data collection
- Geographic extent determined through:
  - Visual surveys
  - Public canvassing at interest sites
  - Local press releases inviting sightings
- Field seasons: 2016–2018 (3 seasons), totaling 1331 sightings across 25 sites.
- Visual surveys:
  - Conducted 07:30–18:00 on sunny days; observers searched basking/refuge habitats
  - Locations recorded with GPS (±1 m) or annotated from aerial imagery
  - Special railway transect at West Worthing, ~9.5 km, with 21 survey points and 11 refugia locations
  - Access constraints influenced survey distribution; refugia left in place for up to a week
- Community engagement:
  - Door-to-door canvassing (2017–2018) within 200 m of known populations
  - 500 postcards mailed; 76 credible sightings reported (15% response rate)
  - Online Participatory GIS (PPGIS) via map-me.org; responses linked to spatial attributes for validation
  - 114 participants engaged; records validated via location, photos, proximity to known populations
- Press outreach:
  - 2017 local press release to broaden distribution and prompt sightings via PPGIS
  - Postings included identification aids and bit.ly/lizarduk link

## Modelling approach

### Climate suitability across the UK (MaxEnt)
- Presence data used from the UK and native ranges; spatial thinning to 10 km to reduce autocorrelation (SpThin).
- Data: 25 UK records; 1,542 native-range records; three modelling scopes tested: UK-only, native-only, and UK+native combined.
- Environmental variables:
  - 10 climatic variables from WorldClim and E-OBS (temperature, insolation, frost/summer days, etc.)
  - Variables downscaled/resampled to cohesive resolutions; correlated variables removed to maximise model performance.
- MaxEnt setup:
  - Regularization multiplier set to 2; linear features only to reduce over-fitting
  - Default settings otherwise; presence/background data provided as SWD files for local projections

### Modelling local habitat suitability
- Local scale: 1083 presence records across 10 study locations (urban, suburban, rural)
- Inputs:
  - 6 environmental variables at 2 m resolution
  - 2 m resolution data prepared in ArcGIS; fine-scale habitat type layers created from Phase One Habitat Survey Toolkit
- Outputs:
  - Relative habitat suitability maps (0–1) for each local site
  - Inputs rescaled to reflect carrying capacity (1–100) and a cost surface (1–10) representing movement resistance
  - All inputs resampled to 15 m × 15 m cells to balance detail with computational efficiency

### Modelling local range expansion (RangeShifter IBM)
- RangeShifter v1.1 used to simulate eco-evolutionary dynamics on the MaxEnt-derived landscapes
- Inputs:
  - Habitat quality (scaled from MaxEnt to 1–100)
  - Cost surface (reciprocal of habitat suitability, scaled 1–10)
- Simulation setup:
  - Initial distribution defined from known introduction points or population centers
  - Extinction probability per cell per year = 0.003
  - 50 replicates per site, simulated to year 2040
- Demographic and behavioural parameters:
  - Sourced from literature and calibrated through iterative runs
  - Includes mating system, fecundity, survival, density dependence, dispersal, perceptual range, and movement rules
  - Table 2 lists specific parameters and literature sources

## Outputs and data products

- RangeShifter outputs by site:
  - <SITE>_pop.csv: per-cell population counts across years and replicates
  - <SITE>_avg.csv: averaged results across 50 replicates
  - Columns include replicate number, year, reproductive season, cell coordinates, age/sex structure, juvenile births, etc.
- Site-level files for model inputs:
  - <SITE>_max_15.txt: MaxEnt local habitat suitability
  - <SITE>_cost_15.txt: Local movement cost surface
  - <SITE>_release.txt: Release location data for simulation initiation
  - Some sites include separate release files (branks_release.txt, canford_release.txt)
- Local site deployment:
  - Site prefixes include bourne, branksome, canford, east, port, abbot, bury, ferrer, folk, shore, wemb, worth
- Supporting raster data:
  - ASC files with study-area specific variables used in local modelling
  - OSGB 1936 / British National Grid coordinates

## Data governance and accessibility

- Data are organized with clear file naming conventions and metadata in accompanying tables (e.g., Table 1–4 references)
- Data quality and provenance are addressed through:
  - Field validation of sightings (location, photos, proximity checks)
  - Iterative parameter calibration for RangeShifter against observed extents
  - Documentation of variable sources and resolutions
- Outputs are structured for reproducibility and re-use in monitoring frameworks, including provision of raw and processed inputs/outputs for modelling

## Implications for monitoring frameworks

- Demonstrates integration of citizen science, field surveys, and formal modelling to monitor invasive species spread and population growth.
- Highlights the importance of data quality, metadata clarity, and transparent data processing in monitoring workflows.
- Illustrates a replicable modelling pipeline (MaxEnt habitat suitability → movement cost layers → RangeShifter IBM) suitable for scenario testing and decision support.
- Emphasizes the need for governance around data sharing, standardization of inputs, and documentation to enable ongoing monitoring and updates.