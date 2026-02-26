# Trees recapture ammonia emissions using shelterbelts: model outputs for Great Britain

- Objective: Assess how downwind tree shelterbelts can recapture ammonia emitted from animal housing, improving animal welfare and environmental outcomes by reducing atmospheric deposition near sensitive habitats. The dataset explores how varying canopy depths/heights and seasonal leafiness (LAI) affect recapture and dispersion.

- Scope and data coverage:
  - GB-wide model output on a 100 by 100 km grid (10,000 km2). Northern Ireland covered by a single 10,000 km2 square.
  - Meteorological inputs from CHESS-met (GB 1961–2017), aggregated to 100 km × 100 km resolution; a typical year is represented by 10 years of data (2008–2017) and four representative days per season.
  - Northern Ireland weather approximated by using the closest GB grid-square on the west coast of Scotland.
  - Tree height varies by grid due to geography, soil, and weather; heights derived from Forest Research DSS tools. Backstop canopy uses a fixed conifer (Sitka Spruce) type.

- Treebelt design and input parameters:
  - Structure: a main canopy (2–4 m spacing, open to allow plume entry) plus a backstop canopy (2 m spacing, thick barrier, evergreen).
  - Main canopy LAI varies with spacing, age, and season; backstop LAI fixed by design.
  - LAI values provided for main canopy across ages (0, 5, 15, 25, 50 years) and seasons (Spring, Summer, Autumn, Winter).
  - Backstop canopy LAI values fixed by year (1–5) with defined heights and depths for main/back canopies.
  - Fixed model geometry: ammonia source area 15 m2, distance from shed to trees 20 m, source particle counts (80,000) and canopy particle counts (800,000).

- Modelling approach and data processing:
  - Dispersion and deposition: MODDAS-2D v2.7.1 (2D Lagrangian Stochastic) coupled with OpenFOAM v1706 for turbulence and canopy physics (Segersson modifications).
  - Coupled via a Python (2.7) coupler.
  - Computations performed on the LOTUS cluster (JASMIN) in parallel to derive ammonia recapture percentages.

- Output and key variables:
  - Recapture metrics: TOTAL_RECAPTURE, MAIN_RECAPTURE, BACK_RECAPTURE (percentages for combined canopy, main canopy only, backstop canopy only).
  - Input/grid identifiers: LATITUDE_WGS89, LONGITUDE_WGS84, SQ_NUMBER (GB grid square ID), YEAR (5, 15, 25, 50 years since planting), TIME (3 am or 3 pm).
  - LAI and canopy descriptors: LAD_MAIN, LAD_BACK (leaf area density), HEIGHT_MAIN, HEIGHT_BACK, DEPTH_MAIN, DEPTH_BACK, LAI_MAIN, LAI_BACK.
  - Additional metadata: SEASON, SDEN (source particle density).

- Data structure and format:
  - File: GB_NH3recapture.csv containing grid-based outputs with columns for season, LAI and height metrics, recapture percentages, particle densities, geographic coordinates, and temporal markers.
  - Data fields explicitly capture both the main canopy and backstop canopy contributions to recapture.

- Quality control and validation:
  - Visual checks of input data; meteorological data mapped and checked.
  - LAI reviewed by Forest Research experts; input-file generation code reviewed by experts.
  - OpenFOAM and MODDAS are peer-reviewed; OpenFOAM supported by a large community.
  - Northern Ireland data sourced from closest GB grid square due to CHESS-met limitations.

- Applications and interpretation:
  - Enables assessment of how different treebelt configurations and seasonal leaf area influence ammonia recapture at a continental scale.
  - Supports planning of farm treebelts to mitigate ammonia impacts on sensitive habitats and inform environmental policy.
  - Provides a framework to compare combined canopy effects with main-canopy-only and backstop-only scenarios.

- Limitations and considerations:
  - Northern Ireland weather data approximated from GB grid-square data.
  - LAI and canopy parameters are modelled with specific species choices and spacing; real-world results may vary with alternative species or local management.
  - Data resolution is grid-based and may not capture micro-scale variations; local validation is recommended for site-specific decisions.

- References:
  - Forrester, D. I., & Tang, X. (2016). Analysing the spatial and temporal dynamics of species interactions in mixed-species forests and the effects of stand density using the 3-PG model. Ecological Modelling.
  - Loubet, B., et al. (2006). A coupled dispersion and exchange model for short-range dry deposition of atmospheric ammonia. Quarterly Journal of the Royal Meteorological Society.
  - Robinson, E. L., et al. (2020). CHESS-met meteorology dataset for Great Britain (1961–2017). NERC Environmental Information Data Centre.
  - Segersson, D. (2017). Tutorial to urban wind flow using OpenFOAM. CFD with OpenSource Software conference.
  - Bealey, W. J., et al. (2014). Modelling agro-forestry scenarios for ammonia abatement in the landscape. Environmental Research Letters.