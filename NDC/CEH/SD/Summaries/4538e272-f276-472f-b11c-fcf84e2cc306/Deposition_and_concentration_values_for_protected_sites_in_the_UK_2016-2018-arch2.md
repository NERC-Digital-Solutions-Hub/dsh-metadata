# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Objective
  - Map deposition and concentration data to UK protected sites to support assessment of environmental health and policy performance over time, using standardized data processing and analysis workflows.

- Modelling approaches
  - CBED (Concentration Based Estimated Deposition): generates 5x5 km resolution maps of wet/dry deposition for sulphur, oxidised and reduced nitrogen, and base cations from air and precipitation measurements (UKEAP network). Wet deposition uses precipitation maps and occult deposition; dry deposition uses deposition velocities across land cover categories (forest, moorland, grassland, arable, urban). Applies to forest and non-woodland habitats accordingly; 3-year rolling means used to smooth inter-annual variability.
  - PCM (Pollution Climate Mapping): produces background maps and 1x1 km grids of pollutant concentrations (NOx, NO2, SO2, PM, etc.) with base year and projection runs; includes road-side values (~9,000 points) and supports scenario assessment and exposure calculations.

- Spatial processing steps
  - Step 1: Create a UK 5x5 km grid; clip to SAC/SPA/SSSI boundaries; merge with 3-year CBED output (2016–2018) to produce a UK protected sites CBED dataset.
  - Step 1 (cont.): Repeat the process for 1x1 km concentration datasets for NOx and SO2 using PCM outputs.
  - Data boundaries and site lists are sourced from each country’s national portals.

- Outputs and data integration
  - For each protected site, compute minimum, maximum, and grid-average deposition/concentration values using SQL on the gridded CBED/PCM data.
  - Grid-average deposition calculation: CBEDDepositionValue × (GridArea / TotalSiteArea), summed across grids within the site.

- CBED modelling details
  - Interpolates site measurements to concentration maps; combines ion concentrations in precipitation with annual precipitation to estimate wet deposition; applies land-cover-specific dry deposition for five grid square land-cover types; depostion to forests vs. moorlands distinguished; includes occult deposition and orographic enhancement for precipitation concentration in uplands (based on observed altitude effects).
  - Recognizes inter-annual variability; 3-year averaging used for deposition estimates when calculating critical-load exceedances.
  - Outputs: per-site 3-year mean values under three ecosystem assumptions (moorland/short vegetation everywhere; forest everywhere; grid-average across ecosystems).

- PCM modelling details
  - Provides 1x1 km background concentration maps for multiple pollutants; used for policy support, TEN applications, exposure assessments, and scenario planning.

- Timeframe and data representation
  - All calculations presented as 3-year means for 2016–2018, with annual data produced but summarized as rolling means; outputs are ecosystem-specific (forest, moorland) and grid-average.

- Data structure and datasets (high-level)
  - Datasets include:
    - 3-year means (2016–2018) deposition by grid for forest and moorland, at 5x5 km resolution.
    - 3-year means concentrations of NH3, NO2, SO2 at 5x5 km or 1x1 km resolutions.
    - Minimum, maximum, and average deposition/concentration values by site (forest/moorland/grid-average) at 5x5 km resolution.
    - 3-year means for NOx, NH3, and SO2 concentrations at 1x1 km resolution, plus 3-year means by ecosystem type.
  - Datasets cover site metadata (SITEAREA, CENTROID coordinates, DESIGNATION), grid overlap (GRIDAREA), and YEAR (mid-year of rolling average).

- Units and interpretation
  - Deposition: keq ha-1 year-1 (convertible to kg S ha-1 y-1 or kg N ha-1 y-1 as needed).
  - Concentrations: µg m-3 for NH3, NOx, and SO2.
  - Total nitrogen deposition is the sum of NO2NO3 and NH3NH4 components; total sulfur deposition combines marine/non-marine components as appropriate.

- Quality control and governance
  - QA follows government model QA practices; extensive peer review and participation in Defra model inter-comparison exercises.
  - Version control, method documentation, and centralized code storage are standard.
  - Mass-balance checks are routinely performed and results are compared across years.

- Data accessibility and reuse
  - Datasets are structured for clear ingestion (by grid, by ecosystem type, and by site) and are designed for upload to appropriate data portals; outputs are presented as maps, charts, and reports for policy scrutiny.

- References and resources
  - Core methodological and observational sources cited (e.g., Holme Moss and Great Dun Fell studies; RoTAP and related Defra methodological papers) and links to dataset repositories and PCM/UKEAP information are provided.