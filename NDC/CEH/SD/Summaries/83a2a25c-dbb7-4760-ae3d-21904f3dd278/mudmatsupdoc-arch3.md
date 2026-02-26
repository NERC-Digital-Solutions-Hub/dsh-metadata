# Dataset for Ammonia recapture by tree shelterbelts downwind of an ammonia source

- Purpose: Provides model-based outputs on how woodland/tree shelterbelts can recapture ammonia emissions from animal housing, potentially dispersing plumes and reducing deposition near sensitive habitats. Designed to inform environmental health monitoring, policy evaluation, and decision-making about nature-based ammonia abatement.

- Spatial and temporal scope:
  - Region: Great Britain (GB) grid of 100 km × 100 km (10,000 km2); Northern Ireland represented by a single 10,000 km2 square.
  - Time representation: CHESS-met meteorology (1961–2017) aggregated to a typical year (2008–2017) to reduce inter-annual variability; seasonal representation using four days from each season.
  - Grid reference: input/output coordinates provided, including latitude/longitude in WGS84.

- Data inputs and environmental context:
  - Meteorology: RH, air temperature, wind speed from CHESS-met; Photosynthetically Active Radiation (PAR) derived from solar radiation data; Northern Ireland weather approximated from the closest GB grid-square.
  - Tree canopy parameters: varying tree heights by grid square (based on soil and weather), LAI values by season and tree age for main canopy; backstop canopy uses a fixed LAI with Sitka Spruce (conifer) as backstop.
  - Treebelt design: two-canopy shelterbelt (main canopy open to allow ammonia entry; backstop dense barrier). Main canopy spacing 2–4 m; backstop spacing ≤ 2 m.
  - Constant model setup: ammonia source area 15 m2, distance from shed to trees 20 m, particle counts (source: 80,000; canopy: 800,000), source density 951 s m−3.

- Modelling approach:
  - Dispersion and recapture models: MODDAS-2D (2D Lagrangian stochastic) for ammonia recapture; OpenFOAM for airflow turbulence; coupled via a Python coupler.
  - Computational setup: runs executed on LOTUS cluster (JASMIN) in parallel; inputs generated from the described data; outputs quantify recapture.

- Output variables and data structure:
  - Key outputs: TOTAL_RECAPTURE, MAIN_RECAPTURE, BACK_RECAPTURE (percentages of recaptured ammonia for the scenario as a whole, main canopy only, backstop canopy only).
  - Season and LAI data: SEASON; LAI_MAIN; LAI_BACK; LAD_MAIN; LAD_BACK; HEIGHT_MAIN; HEIGHT_BACK; DEPTH_MAIN; DEPTH_BACK; and related height-spatial parameters.
  - Spatial and run identifiers: LATITUDE_WGS84; LONGITUDE_WGS84; SQ_NUMBER (GB grid square ID, NI uses a separate scheme); YEAR (5, 15, 25, 50 years since planting); TIME (3am or 3pm).
  - Model specifics: SDEN (source particle density); explicit details for each canopy (MAIN_RECAPTURE, BACK_RECAPTURE) and combined TOTAL_RECAPTURE.

- Data quality and verification:
  - Thorough input data checks; meteorological data mapped and QA’d; LAI data reviewed by Forest Research; input-file generation code reviewed by experts; reliance on peer-reviewed modelling tools (MODDAS-2D, OpenFOAM) with community support.

- Relevance for monitoring frameworks:
  - Provides measurable indicators of ammonia recapture efficiency under different canopy designs, heights, ages, and seasonal conditions.
  - Enables scenario comparison to inform policy on agroforestry/woodland-based ammonia abatement as part of environmental health monitoring.
  - Highlights data needs and governance considerations (metadata quality, data sharing, standardization) when integrating model outputs into monitoring dashboards, reports, or governance processes.

- Considerations and limitations:
  - Northern Ireland weather data approximated from the nearest GB grid-square; inter-annual meteorological variability is reduced by using a typical-year approach.
  - LAI and canopy parameters rely on specific species (e.g., Sitka Spruce for backstop) and model-derived values, which may affect transferability to different regions or species.
  - Data transformation and metadata completeness can influence usability and comparability across monitoring programs.

- References:
  - Forrester, D. I. & Tang, X. (2016). Ecological Modelling.
  - Loubet et al. (2006). QJRMS.
  - Robinson et al. (2020). CHESS-met dataset.
  - Segersson (2017). Tutorial on urban wind flow with OpenFOAM.
  - Bealey et al. et al. (2014). Modelling agro-forestry scenarios for ammonia abatement.