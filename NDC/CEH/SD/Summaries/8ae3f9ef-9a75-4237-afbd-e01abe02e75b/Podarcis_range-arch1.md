# Supporting information for modelling the extent of spatial spread and population growth in introduced populations of a non-native lizard ( Podarcis muralis ) in England

- Purpose and scope
  - Documents data and modelling workflow for assessing spatial spread and population growth of the non-native common wall lizard (Podarcis muralis) in England.
  - Integrates presence and background data with environmental variables to develop habitat suitability (MaxEnt) and to drive spatially explicit population simulations (RangeShifter IBM).

- Data sources and file types
  - Presence and background data for UK and native range:
    - uk_pods.csv (UK records)
    - native_pods.csv (native range records)
    - all_pods.csv (UK + native range combined)
  - Local environmental layers and modelling inputs:
    - Asc raster files (local environmental parameters such as distance to roads) clipped to local study areas.
    - Local SWD (sample with data) inputs for MaxEnt
  - MaxEnt outputs used as inputs to RangeShifter:
    - Local habitat suitability and movement cost layers (.txt files with _max_15.txt and _cost_15.txt prefixes)
    - Release locations for simulations (_release.txt and site-specific variations)
  - RangeShifter outputs:
    - <SITE>_pop.csv: population counts by cell and year
    - <SITE>_avg.csv: averages across 50 replicates
  - Local site and site-specific data files:
    - east_pods.csv, port_pods.csv, abbot_pods.csv, bury_pods.csv, ferrer_pods.csv, folk_pods.csv, shore_pods.csv, wemb_pods.csv, worth_pods.csv (site-specific presence points)
    - local_background_points.csv and local_podarcis_presence.csv (structure and metadata for background/presence points)
  - Additional metadata
    - ASC files for each study area with variables including _ndvi, _phase, _spring, _road, _rail, _build
    - Table 3 and Table 4 datasets describing fields and outputs
    - Figure and workflow illustrating the modelling pipeline

- Data collection and fieldwork
  - Geographic extent assessment conducted across three field seasons (April–September) in 2016–2018.
  - Total of 1,331 lizard sightings across 25 sites (76 online portal, 52 postcard returns, 1,203 visual surveys).
  - Researchers: R. Williams and L. Mendes da Costa (data collation and interpretation).
  - Visual surveys
    - Conducted 07:30–18:00 under sunny conditions; GPS-recorded lizard locations with ±1 m accuracy; supplementary annotation from aerial imagery.
    - West Worthing, Sussex rail corridor surveyed as a 9.5 km linear transect with 21 survey points and 11 refugia locations; multiple visits per point with access limitations reflected in survey frequency.
  - Community engagement
    - Door-to-door canvassing (2017–2018) to confirm absences beyond observed extents.
    - Freepost postcards (500 delivered; 76 credible reports; 52 confirmed locations) and a Participatory GIS portal (PPGIS) for sighting submissions and validation questions.
    - PPGIS engagement: 114 participants; validation based on location accuracy, photos, and proximity to known populations.
  - Public outreach
    - 2017 press release to broader local media to publicize sightings and invite reports via bit.ly/lizarduk.

- Modelling climate suitability across the UK (MaxEnt)
  - Data integration
    - UK presence data combined with native-range records (GBIF 2020); spatial thinning to reduce autocorrelation at 10 km; final dataset: 25 UK records and 1,542 native-range records.
    - Compared three model variants: UK-only, native-range-only, and combined UK + native data.
  - Environmental variables
    - 10 climatic variables selected for relevance to Podarcis muralis biology, drawn from WorldClim and ENSEMBLES (E-OBS), up-scaled to 0.0083° where needed.
    - Covariate reduction to minimize inter-variable correlation (Spearman r_s < 0.6).
  - MaxEnt configuration
    - To reduce overfitting: linear features only; regularisation multiplier set to 2.
    - Local-scale models built with presence and background points (SWD format) and projected onto 10 study sites.
  - Local habitat modelling inputs
    - 1083 presence records from direct observations across 10 study locations (urban, suburban, rural).
    - Fine-scale habitat variables at 2 m resolution (NDVI, distance to buildings/roads/rail, solar insolation, habitat phase, etc.).
    - ArcGIS used for variable calculation; habitat types derived from Phase One Habitat Survey Toolkit.

- Modelling local range expansion (RangeShifter IBM)
  - Data inputs and workflow
    - Outputs from MaxEnt (habitat quality and cost layers) used to drive RangeShifter v1.1 simulations.
    - Habitat quality maps scaled to 1–100 carrying capacity; cost surfaces derived from reciprocal of habitat suitability (1–10) to represent dispersal resistance.
    - All inputs resampled to 15 m × 15 m cells to manage memory while aligning with realistic movement scales.
  - Parameterisation and initialisation
    - Demography and behaviour parameters drawn from published literature; calibration performed per site to align simulations with observed extents.
    - Initial release locations based on known introduction points or population extent center; founder size and age class assigned per site.
    - Local extinction probability set at 0.003 per year for stochasticity.
    - Simulations run for 50 replicates per population, up to the year 2040.
  - Parameter details
    - Table 2 provides species biology and model parameters (sex ratio, lifespan, fecundity, mating system, density dependence, dispersal/emigration, survival probabilities, perceptual range, settlement rules, etc.) with literature sources.
  - Outputs
    - Site-specific outputs include populations and coordinates per cell over time, enabling analyses of spatial spread and population growth trajectories.

- Local site details and data organization
  - Site-specific pod location files (pods.csv) cover locations within Eastbourne, Portland, Newton Abbot, Bury, Newton Ferrer, Folkestone, Shoreham, Wembdon, Worthing, Bournemouth area, and others (as listed in the document).
  - Data organization supports both national-scale assessments and fine-scale local projections.

- Data formats, naming conventions, and metadata
  - File prefixes and suffixes encode site and data type (e.g., _pods.csv for presence points, _max_15.txt for MaxEnt habitat outputs, _cost_15.txt for cost layers, _release.txt for release sites, _pop.csv and _avg.csv for RangeShifter outputs).
  - Local background and presence data structured with fields such as x, y (OSGB/British National Grid), habitat indices (NDVI, phase, insolation), and distance metrics (road, rail, build).
  - ASC raster files organized by study area and variable (e.g., bourne_phase.asc, bourne_road.asc), representing local environmental layers at matching resolutions.

- Outputs and intended use
  - The integrated dataset and modelling workflow enable:
    - National and local predictions of habitat suitability and potential spread.
    - Spatially explicit simulations of population growth and range expansion to 2040.
    - The provision of readily usable datasets (with metadata) for replication, public portals, and further analysis.

- References and methodological grounding
  - Methodological references cover key tools and empirical sources for thinning, niche modelling (spThin, MaxEnt), climate datasets (WorldClim, E-OBS), RangeShifter, and lizard biology literature informing parameter choices and ecological assumptions.