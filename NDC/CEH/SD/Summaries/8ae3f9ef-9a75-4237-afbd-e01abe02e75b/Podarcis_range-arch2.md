# Supporting information for modelling the extent of spatial spread and population growth in introduced populations of a non-native lizard ( Podarcis muralis ) in England

## Purpose and scope
- Documents methods and data used to model spatial spread and population growth of Podarcis muralis in England.
- Integrates field observations, community-reported sightings, and climate/landscape data to drive spatially explicit models (MaxEnt for habitat suitability; RangeShifter for individual-based population dynamics).

## Data sources and datasets
- Presence and background data for P. muralis:
  - uk_pods.csv (UK records)
  - native_pods.csv (native range records)
  - all_pods.csv (UK + native combined)
- Local environmental parameter rasters (Asc format) for various regions (e.g., bourne, east, port, abbot, etc.) representing factors like distance to roads/rails, NDVI, insolation.
- MaxEnt outputs (local habitat suitability models) stored as .txt files used as inputs for RangeShifter.
- RangeShifter inputs and outputs:
  - Local habitat inputs: maxent-derived suitability and corresponding movement cost layers.
  - Population outputs: <SITE>_pop.csv and <SITE>_avg.csv (50 replicates) showing projected population per landscape cell and averages.
  - Site-specific files prefixed with location names (e.g., bourne, worth, east, etc.).
- Location data for local sites and basemaps:
  - east_pods.csv, port_pods.csv, abbot_pods.csv, bury_pods.csv, ferrer_pods.csv, folk_pods.csv, shore_pods.csv, wemb_pods.csv, worth_pods.csv.
- Local background and presence data structure (local_background_points.csv, local_podarcis_presence.csv) with fields for NDVI, habitat phase, insolation, roads, rail, buildings, and coordinates (OSGB/British National Grid).

## Field data collection and community engagement
- Visual surveys across 2016–2018 (three field seasons), totalling 1331 lizard sightings across 25 sites.
- Visual survey methodology:
  - Conducted under suitable weather (sunny periods); GPS coordinates collected to ~±1 m; aerial imagery used for refinement.
  - Special railway transect in West Worthing (June–July 2018) along ~9.5 km with 21 survey points and 11 refugia locations; repeated visits varying by access.
  - Refugia left in place for a week or more where possible; access constraints affected replication.
- Community engagement:
  - Door-to-door canvassing (2017–2018) to confirm absence/presence in residential gardens within 200 m of known populations.
  - Freepost postcards and an online Participatory GIS (PPGIS) portal (map-me.org) to record sightings; 114 participants engaged, 76 credible records.
  - Press releases (2017) disseminated to local outlets to publicize sightings and invite reports via PPGIS and direct contact.

## Modelling framework
- Climate and landscape modelling (MaxEnt):
  - Uses UK presence data and native-range records to build relative habitat suitability maps at national extent.
  - Data thinning to reduce spatial autocorrelation: 10 km minimum distance between points (SpThin).
  - Model comparisons using presence data from UK only, native range only, and combined UK+native.
  - Ten climatic variables selected (from WorldClim and ENSEMBLES) and up-scaled to a common resolution; covariance reduced by removing correlated variables.
  - Model complexity constrained (linear features; regularisation multiplier = 2) to reduce overfitting.
- Local habitat suitability (MaxEnt inputs for 10 study sites):
  - 1083 presence records from visual surveys across urban, suburban, and rural habitats.
  - 2 m resolution inputs for local environmental variables (NDVI, distances to roads/buildings/rail, spring insolation, etc.).
- Local range expansion (IBM with RangeShifter v1.1):
  - Spatially explicit individual-based model simulating life-history and movement on a 15 m × 15 m grid.
  - Inputs derived from MaxEnt outputs: habitat quality (rescaled to 1–100 carrying capacity) and a cost surface (1–10) computed as the reciprocal of habitat suitability.
  - Initial introduction at known site coordinates or population center; multiple replicates (50) run per site; projection to 2040.
  - Local extinction probability per cell per year set to 0.003 to incorporate stochasticity.
- Parameterisation and initialization:
  - Demographic and behavior parameters drawn from literature; calibrated iteratively to reproduce observed current extents.
  - Founder sizes set where known; otherwise minimal size producing plausible outputs; adult age class assumed for founders.
  - Extinction and dispersal dynamics integrated to reflect species biology and landscape structure.

## Outputs and file structure
- RangeShifter outputs:
  - <SITE>_pop.csv: yearly population counts per cell for each replicate.
  - <SITE>_avg.csv: averaged outputs across 50 replicates.
- MaxEnt and ASC inputs:
  - <STUDY_AREA>_<VARIABLE>.asc: raw raster layers for each local region and variable (e.g., bourne_phase.asc, port_road.asc).
  - Local background and presence files contain x,y coordinates (OSGB grid) and associated covariates (NDVI, phase, insolation, distances).
- Site and region naming:
  - 10 study sites include Bournemouth (bourne), Branksome/Branksome area (branksome), Eastbourne (east), Portland (port), Newton Abbot (abbot), Bury (bury), Newton Ferrer (ferrer), Folkestone (folk), Shoreham (shore), and Worthing (worth), with additional local site files per location.
- Data formats and coordinate system:
  - OSGB 1936 / British National Grid coordinates for all spatial points.
  - Outputs include textual (.txt) model outputs and CSV files for population dynamics.

## Parameterisation and initialization details
- Demographics and behavior (Table 2 in the document) drawn from published literature; parameters adjusted to fit observed distributions across 10 study sites.
- Movement and dispersal:
  - Emmigration and step mortality reflect stage- and sex-dependent rules; perceptual range and directional persistence defined; settlement is density-dependent.
- Simulation design:
  - 50 replicates per site, simulating expansion from the introduction point to the year 2040.
  - Acknowledges limitations such as uncertain founder sizes and potential data gaps in early observations.

## Accessibility, reproducibility, and data sharing
- Comprehensive dataset and modelling workflow are bundled with:
  - Presence and background data for UK/native ranges.
  - Local habitat and movement inputs (MaxEnt outputs, ASC rasters).
  - IBM simulations and site-specific outputs.
- The study emphasises standardized data formats (SWD for MaxEnt, clearly named site files, and well-documented variable sources) to enable reuse.
- Community-sourced data (PPGIS) and press outreach demonstrate combining formal surveys with public contributions to enhance monitoring coverage.
- Noted challenges include logistical constraints for refugia deployment, variable data resolution across sources, and the risk of model overfitting despite thinning and constraint strategies.

## Key considerations for environmental monitoring analysts
- Demonstrates an end-to-end workflow for monitoring an invasive species: field surveys, community reporting, climate-informed habitat modelling, and spatially explicit population projections.
- Shows how to harmonize disparate data sources (presence data, environmental rasters, citizen science records) into a coherent modelling framework.
- Provides explicit data/file structures and model parameterization that support reproducibility and potential data sharing across agencies or research teams.
- Highlights the importance of documenting data provenance, spatial resolution, and site-specific assumptions to facilitate scrutiny and policy assessment over time.