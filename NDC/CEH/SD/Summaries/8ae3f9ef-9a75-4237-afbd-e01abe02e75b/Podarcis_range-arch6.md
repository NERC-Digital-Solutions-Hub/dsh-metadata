# Supporting information for modelling the extent of spatial spread and population growth in introduced populations of a non-native lizard ( Podarcis muralis ) in England

## Overview and aims
- Document describes datasets and methods used to model the spatial spread and population growth of the non-native common wall lizard (Podarcis muralis) in England.
- Integrates presence data and environmental data to support MaxEnt habitat suitability modelling at national and local scales, and subsequent population growth and spread modelling with an individual-based model (RangeShifter).

## Data collected and types
- Presence and background data
  - uk_pods.csv (UK records), native_pods.csv (native range), all_pods.csv (UK + native combined): presence inputs for MaxEnt at different extents.
  - Local site files with _pods.csv (e.g., east_pods.csv, port_pods.csv, etc.) containing x/y coordinates in OSGB 1936 grid.
- Field sightings and survey methods
  - 1331 lizard sightings across 25 sites from 2016–2018 (April–September): 76 online portal, 52 postcard returns, 1203 visual surveys.
  - Visual surveys along transects (notably a ~9.5 km railway transect at West Worthing, Sussex) with GPS locations to ±1 m and systematic checks.
- Community engagement and citizen science
  - Door-to-door canvassing (2017–2018) and home visits within 200 m of known populations.
  - Postcards (500 sent; 76 credible sightings; 52 confirmed locations) and an online PPGIS portal for sightings (map-me.org).
  - Validation of PPGIS records using location, photos, proximity to known populations, and respondent answers about behavior and confidence.
- Public communications
  - 2017 press release to broader audience to raise awareness and solicit sightings.

## Modelling data inputs and processing
- Climate and environmental variables
  - 10 climatic variables selected from WorldClim and E-OBS for relevance to wall lizard biology.
  - Data thinning to reduce spatial autocorrelation (10 km spacing) yielding 25 UK presence records and 1542 native-range records for MaxEnt.
  - Local habitat variables prepared at 2 m resolution; NDVI and distance-to-built/roads/rail variables included.
- MaxEnt habitat suitability modelling
  - Local-scale modelling across 10 study sites; 1083 presence records used.
  - Local environmental inputs: 2 m resolution variables (e.g., NDVI, distances to roads/buildings/rail, insolation, etc.).
  - Model settings: linear features only, regularisation multiplier of 2 to reduce over-fitting; SWD (sample with data) presence/background inputs; projections to 10 study sites.
- Local range expansion modelling (RangeShifter IBM)
  - RangeShifter v1.1 used to simulate movement and demography on habitat/ cost surfaces derived from MaxEnt outputs.
  - Inputs include: habitat quality (MaxEnt values rescaled to 1–100) and cost surfaces (reciprocal of habitat suitability, 1–10), resampled to 15 m cells.
  - Initial release sites identified from introduction data; 50 replicate simulations per population through to 2040.
  - Demographic and behavioral parameters drawn from literature and calibrated to fit observed extents; stochastic extinction probability set to 0.003 per year.
- Local and national data modeling structure
  - Local ASCII rasters (asc) and SWD files per site feed RangeShifter inputs.
  - Outputs include per-cell population data and coordinates for local growth and spread.

## File structure and outputs
- Local model inputs and outputs
  - Local background/presence data: local_background_points.csv and local_podarcis_presence.csv (structure includes species, IDs, NDVI, phase, spring insolation, distances to roads/rails/buildings, x/y coordinates).
  - Local MaxEnt outputs: <SITE>_max_15.txt (habitat suitability), <SITE>_cost_15.txt (movement cost), <SITE>_release.txt (release locations).
  - Local site identifiers include bourne, east, port, abbot, bury, ferrer, folk, shore, wemb, worth (and branksome/canford as separate releases).
- Simulation results
  - <SITE>_pop.csv: per-year, per-cell population data (NInd, stage counts, juveniles, coordinates, year).
  - <SITE>_avg.csv: 50 replicate averages for the same metrics.
- Local study ASCII rasters
  - Files named <STUDY_AREA>_<VARIABLE>.asc (e.g., bourne_phase.asc, bourne_road.asc), covering variables such as _ndvi, _phase, _spring, _road, _rail, _build, with resolutions typically 2 m (or 0.25–2 m depending on variable).
- Tables and data descriptions
  - Table 1: list of environmental variables used in national/local MaxEnt models.
  - Table 2: ranges and sources for demographic and life-history parameters used in RangeShifter (with explicit and literature-derived values).
  - Table 3: structure description for local input files local_background_points.csv and local_podarcis_presence.csv.
  - Table 4: structure description for <SITE>_pop.csv and <SITE>_avg.csv outputs.
- Formats and references
  - Outputs include .csv, .txt, and .asc files; all OSGB/British National Grid coordinates used.

## Software and methodological tools
- MaxEnt v3.3.3k for species distribution (habitat suitability) modelling.
- RangeShifter v1.1 for spatially explicit individual-based population modelling.
- spThin R package used to reduce spatial autocorrelation by thinning presence records (min distance 10 km).
- ArcGIS for processing climate/environmental variables and creating fine-scale habitat layers.
- Aerial imagery and lidar-based inputs for high-resolution environmental variables.
- PPGIS and GIS-based validation methods to corroborate citizen science data.

## Biological rationale and parameterization
- Podarcis muralis demonstrates rapid adaptation to cool climates and changes in thermal tolerance, informing model design.
- Local-scale modelling links habitat suitability to carrying capacity and movement cost, enabling simulation of range expansion under different landscape contexts.
- Parameterization draws from published literature; where data are unavailable, reasonable biologically realistic assumptions are used and iteratively calibrated to match observed extents.

## Access and interpretation considerations
- Data integrate traditional field surveys with citizen science and media-derived sightings to cover a broader spatial extent.
- Validation steps emphasize supporting evidence (location, photographs, proximity to known populations, consistency of responses).
- Model outputs provide detailed spatial-temporal projections of population growth and spread, useful for management planning and understanding invasion dynamics.

## References and supporting sources
- Includes citations for spThin, RangeShifter, WorldClim, E-OBS, GBIF, Langham 2019, Michaelides et al. 2015/2016, and other foundational studies informing lizard biology and modelling approaches.