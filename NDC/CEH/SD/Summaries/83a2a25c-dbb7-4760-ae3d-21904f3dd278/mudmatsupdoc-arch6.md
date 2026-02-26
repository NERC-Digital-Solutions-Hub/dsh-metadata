# Trees have the potential to recapture ammonia emissions...

- Purpose and scope
  - Dataset of model outputs for different scenarios where treebelts are situated downwind of an ammonia source in Great Britain.
  - Aims to show how existing woodland or new plantings (farm treebelts) can reduce ammonia concentrations and atmospheric deposition near sensitive habitats, while aiding dispersion and recapture by canopies.
  - Outputs include percentages of ammonia recapture under various canopy designs, heights, ages, and seasonal conditions.

- Data coverage and structure
  - Spatial: Great Britain divided into a grid of 100 by 100 km (10,000 km2). Northern Ireland covered by a single 10,000 km2 square. Data points identified by latitude/longitude in WGS84; grid square ID (SQ_NUMBER) provided (GB; NI treated as one square).
  - Temporal and seasonal: runs include seasons (winter, spring, summer, autumn) with four representative days per season to capture seasonal variation.
  - Tree/calibration years: trees planted years 5, 15, 25, or 50; corresponding LAI values provided. For main canopy, LAI varies by season and age; backstop canopy LAI fixed across years.
  - Output fields include TOTAL_RECAPTURE, MAIN_RECAPTURE, BACK_RECAPTURE, along with associated metadata (LAI_MAIN, LAI_BACK, HEIGHT_MAIN, HEIGHT_BACK, DEPTH_MAIN, DEPTH_BACK, LAD_MAIN, LAD_BACK, SDEN, YEAR, TIME).

- Input data and meteorology
  - Meteorological data derived from CHESS-met (1961–2017), aggregated to 100 km resolution and then represented by four days per season from 2008–2017 to create a typical year.
  - Local weather variables used: relative humidity, air temperature, wind speed; Photosynthetically Active Radiation (PAR) derived from shortwave radiation.
  - Northern Ireland weather data applied from the closest GB grid-square on the west coast of Scotland.

- Tree design and LAI details
  - Treebelt design: main canopy (2–4 m spacing, open to allow plume entry) at the front of the shelterbelt; backstop canopy (conifer, evergreen) with tight spacing (2 m or less) to form a barrier.
  - Main canopy LAI: seasonal values provided for 0, 5, 15, 25, 50-year-like ages, reflecting spacing at 2.5 m and seasonal variation (Spring, Summer, Autumn, Winter).
  - Backstop canopy LAI: constant values by year (1: 0, 2: 5.2, 3: 6.3, 4: 5.3, 5: 6.1) and 2 m spacing; based on Sitka Spruce for conifers.
  - Height and growth: grid-square-specific tree heights derived from Forest Research DSS tools; NI heights estimated with non-public tools; atypical heights discarded for efficiency.
  - Species assumptions: Sitka Spruce (conifer) as backstop; Aspen (broadleaf) used for LAI tables in model inputs.

- Modeling approach
  - Dispersion and deposition model: MODDAS-2D (2D Lagrangian Stochastic) for ammonia recapture calculation.
  - Turbulence input: OpenFOAM v1706 (with Segersson canopy adjustments) providing turbulence input to MODDAS.
  - Coupling and computation: a Python 2.7 coupler connects MODDAS and OpenFOAM; computations run on the LOTUS cluster (JASMIN) in parallel.

- Constant variables across runs
  - Ammonia source area: 15 m2.
  - Distance from source to trees: 20 m.
  - Source particles: 80,000; canopy particles: 800,000.
  - Ammonia source density: 951 s m-3.

- Data quality and validation
  - Visual QA of input data and QA checks of meteorological mapping; LAI reviewed by Forest Research experts.
  - Input file generation code reviewed by experts.
  - Use of peer-reviewed models (MODDAS-2D, OpenFOAM) with an active user community; OpenFOAM segmentation aligned with Segersson modifications.

- Data structure and fields
  - Seasonal and run descriptors: SEASON; TIME (3 am or 3 pm).
  - Canopy descriptors: LAD_BACK, LAD_MAIN (leaf area density), HEIGHT_MAIN, HEIGHT_BACK, DEPTH_MAIN, DEPTH_BACK, LAI_BACK, LAI_MAIN.
  - Recapture metrics: TOTAL_RECAPTURE, MAIN_RECAPTURE, BACK_RECAPTURE.
  - Source and location: SDEN (source particle density), LATITUDE_WGS84, LONGITUDE_WGS84, SQ_NUMBER.
  - Temporal: YEAR (5, 15, 25, or 50 years since planting).

- How to use and potential applications
  - Enables exploration of how different treebelt configurations influence ammonia recapture and dispersion across GB.
  - Useful for policymakers, environmental planners, and researchers assessing nature-based ammonia abatement and its environmental and social impacts.
  - Supports scenario comparison across seasons, tree ages, canopy designs, and spatial locations, with self-serve tools via the provided dataset outputs.

- References
  - Forrester, D. I. & Tang, X. (2016). Ecological Modelling.
  - Loubet et al. (2006). QJRMS.
  - Robinson et al. (2020). CHESS-met dataset, NERC EIDC.
  - Segersson (2017). Tutorial on urban wind flow with OpenFOAM.
  - Bealey et al. (2014). Environ. Res. Lett.