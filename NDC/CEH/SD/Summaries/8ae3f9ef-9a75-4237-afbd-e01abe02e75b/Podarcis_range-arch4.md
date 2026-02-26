# Supporting information for modelling the extent of spatial spread and population growth in introduced populations of a non-native lizard ( Podarcis muralis ) in England

- Aim of the data: Provide and describe datasets and modelling inputs used to assess spatial spread and population growth of the non-native wall lizard Podarcis muralis in England, at local and national scales, for MaxEnt habitat suitability modelling and RangeShifter individual-based modelling (IBM).

- Data sources and types
  - Presence and background point data for UK, native range, and combined datasets (uk_pods.csv, native_pods.csv, all_pods.csv) used as inputs for MaxEnt habitat suitability models.
  - Local environmental rasters (asc files) representing parameters such as distance to roads, rail, buildings, NDVI, solar insolation, etc., used to derive landscape layers for RangeShifter.
  - RangeShifter outputs: Pop.csv and avg.csv provide projected population sizes and spatial coordinates across landscape cells for 50 replicates per site.
  - Local site coordinates and background/presence data (local_background_points.csv, local_podarcis_presence.csv) with variables including NDVI, habitat phase, insolation, and proximity to roads/rail/buildings.
  - Localized ASCII rasters and SWD (samples with data) inputs for 10 UK study sites (bourne, east, port, abbot, bury, ferrer, folk, shore, wemb, worth).

- Data collection and citizen science engagement
  - Geographic extent determined from three-field-season collaboration (2016–2018): visual surveys, public canvassing, and press releases.
  - Total sightings: 1331 across 25 sites; sources included online portal, postcard returns, and visual surveys; coordinators: R. Williams and L. Mendes da Costa.
  - Visual surveys: GPS-located sightings with ±1 m accuracy; transects along railway in West Worthing (9.5 km) with 80 artificial refugia and multiple survey points; access constraints influenced sampling.
  - Public engagement: door-to-door canvassing (2017–2018) with postcards and an online Participatory GIS (PPGIS) via map-me.org for sighting validation and additional questions to assess reliability.
  - Validation: reported sightings cross-checked for location accuracy, photographic evidence, proximity to known populations, and site visits; 114 users engaged online, with 76 credible sightings.
  - Media outreach: 2017 press release to broaden distribution and invite sightings through the online portal or direct contact with lead researchers.

- Climate suitability and modelling approach
  - Climate/habitat suitability mapped using MaxEnt v3.3.3k, comparing models built from UK introduced-range data, native-range data, and combined datasets.
  - Spatial thinning to reduce autocorrelation: 10 km minimum distance using SpThin; resulting samples: 25 UK records and 1,542 native-range records.
  - Environmental variables: 10 climatic variables derived from WorldClim and E-OBS, with resolution harmonization (0.0083°) and correlation reduction (r_s < 0.6) to optimize model performance.
  - MaxEnt setup to reduce overfitting: linear features only, regularisation multiplier set to 2.

- Local habitat suitability modelling details
  - 1083 presence records from 10 study locations (urban to rural) used to generate relative habitat suitability maps.
  - Local inputs comprised 6 environmental variables at 2 m resolution (NDVI; distances to buildings, roads, rail; Spring insolation; and habitat type), prepared in ArcGIS; additional habitat classification data from Phase One toolkit.

- RangeShifter individual-based modelling (IBM)
  - Habitat inputs: MaxEnt outputs converted to habitat quality (rescaled 0–100 carrying capacity) and cost surfaces (1–10 hostility) to drive movement and survival in RangeShifter.
  - Spatial resolution: resampled to 15 m × 15 m cells to balance memory use and ecological relevance.
  - Initialization: known introduction sites or centers of current sighting extents; founder size per site; adult age class assumed for founders; stochastic local extinction probability (0.003 per year).
  - Simulation design: 50 replicates per population, running from introduction to 2040.
  - Parameterisation: demographic and behavioural parameters drawn from literature; iterative calibration to align outputs with observed extents; where data were lacking, reasonable, biologically plausible assumptions were used.
  - Documentation: Table 2 lists parameters (sex ratio, fecundity, maturation, survival, movement, density dependence, emigration, perceptual range, etc.) with sources.

- Local site data and outputs
  - Site-specific data files organized by location (e.g., bourne, east, port, abbot, bury, ferrer, folk, shore, wemb, worth); local outputs include:
    - <SITE>_max_15.txt and <SITE>_cost_15.txt: MaxEnt habitat suitability and movement cost layers for the site.
    - <SITE>_release.txt: initial release location(s) for simulations.
    - <SITE>_pop.csv and <SITE>_avg.csv: RangeShifter results per replicate, including yearly population counts, subpopulation structure, and geographic coordinates (X, Y) in OSGB British National Grid.
  - Summary structure: Rep, Year, RepSeason, NInd, Nfemales_stage1, Nmales_stage1, Nfemales_stage2, Nmales_stage2, juvenile counts, coordinates, and projected year fields.

- Geographic data and file formats
  - Coordinate reference: OSGB 1936 / British National Grid (BNG) used for all site-level coordinates.
  - ASC and CSV formats: ASCII raster files for local variables; CSV and TXT formats for presence, background, model inputs/outputs, and release points.

- Data governance and reproducibility
  - Clear provenance: multiple data streams (field surveys, public canvassing, PPGIS, press releases) with validation steps described.
  - Versioned modelling workflow: MaxEnt habitat suitability maps feeding into RangeShifter IBM; explicit description of data thinning, variable selection, and parameter calibration to reproduce results.
  - Rich metadata and documentation: detailed table descriptions for input/output files (Tables 1–4 in the document) and comprehensive references to data sources (WorldClim, ENSEMBLES, GBIF, OS maps, Landsat, etc.).

- References and foundational data sources
  - Cited methods and data sources for thinning, climate variables, habitat inputs, movement modelling, and population dynamics (e.g., spThin, WorldClim, ENSEMBLES, GBIF, RangeShifter, MaxEnt).
  - Literature supporting lizard ecology and modelling parameters (reproduction, survival, movement, density dependence, etc.).

- Key takeaways for data leaders
  - The study demonstrates end-to-end data integration from field observations and citizen-science contributions to high-resolution habitat and movement modelling.
  - It highlights data management practices for multi-source ecological datasets, including quality checks, validation workflows, and careful handling of spatial autocorrelation and resolution differences.
  - The modelling pipeline combines correlative (MaxEnt) and mechanistic (RangeShifter IBM) approaches to project future invasion dynamics under heterogeneous landscapes.
  - Outputs are disseminated through a structured file system with site-specific inputs/outputs to enable reproducibility and cross-site comparison, while maintaining clear data lineage and metadata.