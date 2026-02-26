# CBED and PCM Modelling for UK Protected Sites (2015-2017)

- A data pipeline mapping deposition and pollutant concentrations to UK protected sites (SAC, SPA, SSSI) using CBED and PCM outputs, focused on 2015–2017 rolling means.
- Data products are produced on two spatial grains: 5x5 km grids for site-area deposition, and 1x1 km grids for pollutant concentrations.

## Data Processing Pipeline

- Step 1: Spatial mapping
  - Create a 5x5 km UK grid and clip to protected-site boundaries to produce a gridded dataset for SAC/SPA/SSSI.
  - Merge with 3-year averaged CBED deposition data (2015–2017) to yield a UK protected sites CBED dataset.
  - Repeat for 1x1 km NOX and SO2 concentration data from PCM.
  - Source boundary and feature data from national websites.
- Step 2: Derive per-site statistics
  - Use SQL on the gridded data to compute minimum, maximum, and grid-average deposition/concentration for each protected site.
  - Grid-average: Grid square area fraction within the site multiplied by the CBED deposition value, then summed to the site.

## Modelling Approaches

- CBED Modelling
  - Generates 5x5 km resolution maps of wet/dry deposition for nitrogen, sulphur, and base cations from air concentrations and precipitation.
  - Wet deposition combines gas/particle inputs with precipitation and occult deposition; incorporates orographic enhancement for uplands.
  - Dry deposition uses habitat-specific deposition velocities across five land-cover types (forest, moorland, grassland, arable, urban).
  - Outputs include deposition to forest/woodland, moorland, or grid-average ecosystems; time-variability smoothed with rolling 3-year means.
  - Units: keq ha-1 year-1; conversions to kg S ha-1 year-1 or kg N ha-1 year-1 via factors (S: 16, N: 14).
  - Purpose: support critical-load exceedance analyses and ecosystem-specific deposition assessments.
- PCM Modelling
  - Produces background pollutant concentrations on a 1x1 km grid (and road-side representativity) for the UK.
  - One model per pollutant (e.g., NOx, NO2, SO2, PM10, etc.) with base-year and projection runs.
  - Used for policy development, exposure calculations, and TEN (Time Extension Notification) support.

## Data Outputs and Structures

- Datasets span 12 items, with 3-year means (2015–2017) and various aggregates:
  - 5x5 km grid deposition by ecosystem type (forest/moorland) and grid average.
  - 1x1 km grid concentrations for NOx and SO2.
  - Site-level deposition data: minimum, maximum, and average values for forest, moorland, and overall grid-average depostion.
  - Site-level concentration data: NH3/NH4, NO2/NO3, SO2/SO4, including grid-average, minimum, maximum, and average values.
  - Datasets 1–3 describe 5x5 km deposition grids by ecosystem (forest or moorland) and grid-average totals.
  - Datasets 4–6 provide 1x1 km concentration grids for NH3, NO2, SO2 (and related fields).
  Dataset 7–12 contain site- or grid-averaged deposition/concentration values (min/max/avg) for forest or moorland, 3-year means.
- Key fields across datasets
  - SITECODE, SITENAME, SITEAREA, CENTROID_X, CENTROID_Y, COUNTRY, DESIGNATION, YEAR, GRIDAREA.
  - Deposition fields: NH3/NH4, NO2/NO3, SO2/SO4 (in keq ha-1 year-1) and their wind-down conversions.
  - Concentration fields: NH3_CONC, NO2_CONC, SO2_CONC (in µg m-3).
- Timeframe and averaging
  - All data are annual calculations presented as rolling 3-year means (2015–2017) to smooth inter-annual variability.
  - Outputs support ecosystem-specific assessments (moorland vs forest/woodland) and combined grid-average scenarios.

## Data Quality, Standards, and Provenance

- Methods and data have undergone extensive peer review and model inter-comparison processes (e.g., Defra QA, CBED inter-comparison).
- Documentation practices include version control, centralized code storage, and mass-balance checks for numerical consistency.
- Data sources and supporting information are maintained by Defra and related UK atmospheric pollutant programs (e.g., UKEAP, PCM).

## Practical Implications for Data Leaders

- End-to-end data lifecycle demonstrated: data acquisition, GIS processing, SQL-based aggregation, modelling (CBED/PCM), and structured data products for policy-relevant analyses.
- Clear data governance cues: standardized 3-year means, explicit units and conversion factors, and comprehensive metadata descriptors.
- Useful for evaluating data coverage, quality, and gaps across protected sites, and for informing collaboration with the wider data community on environmental monitoring and policy support.