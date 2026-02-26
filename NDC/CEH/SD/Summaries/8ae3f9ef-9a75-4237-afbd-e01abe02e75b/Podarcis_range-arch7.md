# Supporting information for modelling the extent of spatial spread and population growth in introduced populations of a non-native lizard ( Podarcis muralis ) in England

- Overview
  - Aids modelling the extent of spatial spread and population growth of the non-native common wall lizard (Podarcis muralis) in England.
  - Combines presence data, environmental variables, and landscape inputs for local and national scale modelling with MaxEnt, and uses RangeShifter for individual-based population modelling.
  - Outputs include habitat suitability, movement cost layers, and simulated population dynamics across landscape cells.

- Data and datasets
  - Presence and background points for MaxEnt and RangeShifter inputs:
    - uk_pods.csv (UK records)
    - native_pods.csv (native range records)
    - all_pods.csv (UK + native range combined)
    - Local site files with point coordinates in OSGB 1936 / British National Grid:
      - east_pods.csv, port_pods.csv, abbot_pods.csv, bury_pods.csv, ferrer_pods.csv, folk_pods.csv, shore_pods.csv, wemb_pods.csv, worth_pods.csv
  - Local background and presence structures:
    - local_background_points.csv
    - local_podarcis_presence.csv
    - Structure includes fields like _ndvi, _phase, _spring, _road, _rail, _build, x, y
  - ASCII raster inputs (OSGB 2936 / British National Grid):
    - bourne_phase.asc, bourne_ndvi.asc, bourne_road.asc, bourne_rail.asc, bourne_build.asc, and similarly for east, port, abbot, bury, ferrer, folk, shore, wemb, worth
    - Variables include phase, ndvi, spring, road, rail, build, and in some areas insolation
  - Maximum Entropy (MaxEnt) inputs and outputs:
    - <SITE>_max_15.txt (MaxEnt model outputs for local habitat suitability)
    - <SITE>_cost_15.txt (local cost surface for movement)
    - <SITE>_release.txt (location of local release site)
  - RangeShifter (IBM) inputs and outputs:
    - 50 replicates per site
    - <SITE>_pop.csv and <SITE>_avg.csv (population counts by cell and replicates)
  - Localized species occurrence data (table and figures referenced in text)
  - Summary names for sites (prefixes indicate study area):
    - bourne, branksome, canford, east, port, abbot, bury, ferrer, folk, shore, wemb, worth
  - Table and file structures:
    - Table 3: local_background_points.csv and local_podarcis_presence.csv structures
    - Table 4: <SITE>_pop.csv and <SITE>_avg.csv structures

- Modelling and workflow
  - Climate and habitat suitability modelling with MaxEnt v3.3.3k
    - Data thinning to 10 km to reduce spatial autocorrelation (25 UK records, 1542 native-range records)
    - Compare models using UK records only, native-range records only, and UK+native combined
    - Ten climatic variables from WorldClim and E-OBS; resolution adjustments applied (0.0083° for WorldClim, 0.25° for some E-OBS variables)
    - Model complexity controlled: linear features only, regularisation multiplier of 2
  - Local habitat suitability modelling
    - 1083 presence records across 10 study locations
    - 6 environmental variables used at 2 m resolution (plus fine-scale habitat type layers)
    - Variables include NDVI, distance to buildings/roads/rail, spring insolation, and habitat type
    - Outputs used to create habitat quality layers (rescaled to 1–100) and movement cost layers (1–10), then resampled to 15 m for RangeShifter
  - Transition to RangeShifter (IBM)
    - Uses MaxEnt-derived habitat quality and cost layers as inputs
    - Initial population distributed to a single cell per population, based on introduction location or population center
    - Parameterisation drawn from empirical literature; iterative calibration to match current observed extents
    - Stochastic elements: local extinction probability (0.003 per year)
    - Simulations run for the period since introduction up to 2040, with 50 replicates
  - Parameterization and sites
    - Table 2 (not fully shown) documents life-history and behavioral parameters (sex ratio, survival, fecundity, dispersal, density dependence, etc.)
    - Local release locations and founder sizes used where available; otherwise minimal founder sizes chosen to yield reasonable outputs

- Data quality, scope, and field methods
  - Field surveys (2016–2018) across 25 sites; total of 1331 lizard sightings (76 online portal, 52 postcard returns, 1203 visual surveys)
  - Visual surveys conducted 07:30–18:00, GPS-recorded lizard locations within ±1 m
  - Focused transect study along a rail corridor in West Worthing (approx. 9.5 km) with artificial refugia placements
  - Community engagement to validate distributions:
    - Door-to-door canvassing and home visits within 200 m of known locations
    - Postcards (500 delivered; 76 credible responses; 52 confirmations)
    - Participatory GIS (PPGIS) via map-me.org for sighting submissions and questionnaire attributes
    - Validation included location accuracy, photographic evidence, proximity to known populations
  - Public releases (press) used to broaden reporting and validation

- Outputs and interpretation for GIS use
  - MaxEnt outputs: local habitat suitability rasters and probability-based inputs
  - Local cost surfaces: movement resistance maps for RangeShifter
  - Population dynamics: 50 replicate simulations per site, with Pop.csv and avg.csv capturing yearly, seasonal, and spatial distribution data
  - Site-level and regional outputs facilitate assessment of potential spread and growth under various climate and landscape scenarios

- Study sites and coverage
  - Ten study locations for local modelling: Bournemouth (bourne), Branksome (branksome), Canford (canford), Eastbourne (east), Portland (port), Newton Abbot (abbot), Bury (bury), Newton Ferrer (ferrer), Folkestone (folk), Shoreham (shore), Wembdon (wemb), Worthing (worth)
  - Local site files with granular sighting coordinates and background data accompany national-scale inputs

- Reproducibility and references
  - Data processing steps include spatial thinning (spThin), GIS-based variable preparation (ArcGIS, Landsat-derived NDVI, Lidar-based insolation), and standard MaxEnt/R-based methods
  - Key references cited for methods and data sources, including spThin, WorldClim, ENSEMBLES, RangeShifter, and relevant lizard ecology studies

- Notes on limitations and assumptions
  - Autocorrelation and sampling bias mitigated through thinning and careful site selection
  - Ground-truthing conducted for records extending known extents
  - Access constraints (e.g., railway corridor) influenced sampling design and refugia deployment
  - Some parameter values derived from literature or reasonable assumptions where empirical data were lacking