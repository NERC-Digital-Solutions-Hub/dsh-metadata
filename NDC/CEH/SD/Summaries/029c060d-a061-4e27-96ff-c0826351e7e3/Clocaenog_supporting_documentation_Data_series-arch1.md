# Climoor field site in Clocaenog forest Supporting documentation for data

- A climate-change manipulation experiment (Climoor) using automated roof technology to create drought and warming treatments reflecting 20–30 year climate projections.
- Location: Clocaenog Forest, North East Wales; upland wet moorland ecosystem dominated by Calluna vulgaris (heather) with other shrubs and bryophytes.
- Established: 1998; features replicated drought and warming treatments plus control plots to mirror shading from experimental structures.
- Primary aim for analysts: enable data-driven analysis of correlations and predictions on climate-change treatments’ ecosystem responses.

## Site and treatments

- Ecosystem and climate context
  - Upland moorland with Calluna vulgaris >60% biomass; soils are humo-ferric podzols with variable eluvial illuvial horizons.
  - Growing season roughly June–August; shoulders April–May and Sep–Oct; dormancy Nov–Feb.
- Treatments and replication
  - Drought and warming treatments, each with three replicates (4 m x 5 m plots); plus three scaffold-mirrored control plots (total n=9).
  - Drought: historically May–Sept (1999–2011); reduced site rainfall by ~20% (and excluded ~80% of rain during drought periods); since 2012, drought operated April–October.
  - Warming: retractable aluminium curtains to reduce night-time heat loss; rainfall reduction during warming events mitigated by retraction after rain; ~14% annual rainfall reduction on average.
  - Wind constraints: curtains not operated in winds >10 m/s to prevent damage.
- Site-scale climate context (1997–2014 data summarized)
  - Mean air temperature around 8.0°C; mean soil temperature in controls ~7.5°C; mean annual rainfall ~1411 mm; N-deposition ~20–25 kg N ha⁻¹ yr⁻¹.
- Appendix references
  - Plot and quadrat layouts; lysimeters, pin-quadrat layout, and biomass sampling areas.

## Data collection, processing and management

- Data collection infrastructure
  - On-site automated weather station (AWS) for meteorology; multiple plot-level sensors (micro-meteorology); soil, vegetation, and biogeochemical measurements across treatments.
  - Long-running data streams including weather, rainfall, soil respiration, trace gases, net ecosystem exchange, vegetation structure, litter, root biomass, soil chemistry, and more.
- Datasets and time coverage
  - AWS meteorological data: daily, 1999–present; high-frequency (minute- to hourly-averaged).
  - Micro-meteorological data: daily plot-level soil/air temperature and soil moisture; depuis 1998–present.
  - Rainfall and rainfall chemistry: site-level storage rain gauge and biweekly sampling; throughfall data for plots (1998–present with variable completeness).
  - Soil and ecosystem biogeochemistry: soil respiration (fertile history 1999–present with various instrumentation), trace gases (CH4, N2O), net ecosystem CO2 exchange (NEE) across select years, photosynthesis, vegetation biomass surveys, canopy reflectance, phenology, litterfall, root biomass, soil microbial biomass, nitrogen mineralisation, SOM/SOC and bulk density, soil solution and leachate chemistry.
- Data processing and unit conventions
  - Soil respiration and NEE data standardized to mg CO2-C m⁻² hr⁻¹ using cross-instrument conversions (e.g., CIRAS-2 and LICOR 8100 systems) with explicit conversion factors.
  - Throughfall-derived plot rainfall estimates adjusted from plot-level to site-level using percent differences relative to rainfall gauges; handling of missing data via exclusion or year-specific infill with site-wide averages.
  - Pin-quadrat vegetation biomass derived from pin hits using species-specific calibration factors; biomass expressed g m⁻² after conversion.
  - Canopy reflectance indices calculated from spectrometer data: NDVI680, NDVI570, and PRI.
- Quality assurance and documentation
  - Data quality control performed visually and through basic QA checks; note that some legacy data may not follow current best practices.
  - Data sources and datasets are catalogued; some data stored in the EIDC with metadata; contact CEH Bangor for access and details.
- Usage and accessibility challenges (noted for analysts)
  - Data exist at multiple scales (plot-level to site-level) and across numerous formats; varying data completeness over time.
  - Some data (especially older micro-meteorological and soil datasets) may be incomplete or inconsistently documented.
  - IT and data access considerations are common (legacy formats, need for cross-dataset harmonization, and metadata curation).
  - The document emphasizes tracking data sources, ensuring discoverability, and providing clear metadata for reuse.

## Key data streams and typical variables (high-level)

- Climate and weather
  - AWS meteorological measurements: temperature, humidity, rainfall, wind, net radiation, PAR, solar radiation, pressure; daily to hourly timescales.
  - Micro-meteorological measurements: plot-level soil temperature, soil moisture; daily to hourly timescales.
- Hydrology and rainfall chemistry
  - Storage rain gauge: site-level rainfall (biweekly); rain chemistry (pH, NO3, Cl, SO4, DOC, NH4).
  - Throughfall: plot-level rainfall (biweekly); used to derive % reductions per treatment.
  - Water table depth: permeable tubes; biweekly measurements (2009–present).
- Biogeochemistry and soil processes
  - Soil respiration: CO2 efflux from plots (fortnightly and automated campaigns from 2013 onwards); unit conversions to mg CO2-C m⁻² hr⁻¹.
  - Trace gases: CH4 and N2O fluxes from collars using closed-chamber approaches; sample timings at 0.25, 15, and 30 minutes.
  - Net ecosystem CO2 exchange (NEE): chamber-based flux measurements (2002–2004, 2009–2011) with plant biomass adjustments.
  - Photosynthesis: infrequent measurements using CIRAS-2 and leaf cuvettes for selected years/species.
- Vegetation and structure
  - Vegetation surveys (pin-point method) for biomass and cover; species-specific conversion factors; multi-year data (1998–2012, with some years missing).
  - Canopy reflectance: NDVI and PRI indices from ground-based spectrometry (2001–2004, with gaps).
  - Phenology and growth: shoot elongation, budburst, leaf emergence, sex-specific phenophases for Calluna vulgaris, Vaccinium myrtillus, and Empetrum nigrum.
  - Litterfall and litter chemistry; root biomass; soil microbial biomass; nitrogen mineralisation; SOM/SOC and bulk density; soil solution chemistry.
- Data products and metadata
  - Datasets named in the document (e.g., daily AWS data, Rainfall_Clocaenog, Throughfall_Clocaenog, Net ecosystem exchange_Clocaenog, etc.).
  - Supporting documentation available for each dataset; primary contacts for data access (e.g., Sabine Reinsch, Bridget Emmett at CEH Bangor).

## Practical considerations for data-driven analyses

- Potential correlations to explore
  - Drought and warming treatments vs. soil respiration, NEE, CH4/N2O fluxes, and plant biomass dynamics.
  - Relationships between canopy reflectance indices and vegetation phenology, biomass, and photosynthetic activity.
  - Interactions between soil moisture/temperature (micro-meteorology) and biogeochemical processes (mineralisation, SOM/SOC dynamics, nitrogen fluxes).
  - Rainfall regime (throughfall vs. site rainfall) and leachate chemistry, groundwater/water table depth dynamics.
- Modeling and data preparation notes
  - Multiple data sources with differing temporal resolutions require alignment (e.g., daily AWS vs. hourly plot data vs. monthly leachate chemistry).
  - Legacy data processing steps may need re-documentation or reprocessing to ensure reproducibility.
  - Clear documentation of unit conversions and data processing rules is essential for cross-dataset integration.
- Data availability and contact
  - Some data are stored with metadata in portals (EIDC); for access or more details, contact CEH Bangor researchers listed in the document.

## Appendices and site layout

- Appendix 1: Site layout and plot references (grid and coordinates).
- Appendix 2: Quadrat layout for vegetation measurements.
- Appendix 3: Plot layout with quadrats and measurement areas.
- 2012 Climoor plot layout and abbreviations for sampling locations (LYS, PQ, SS).

- Overall, the document provides a comprehensive, multi-decadal, multi-parameter data framework from a drought and warming manipulation experiment in a upland moorland, with explicit methods, data types, and processing notes to enable correlation analyses and predictive modeling by data-focused analysts.