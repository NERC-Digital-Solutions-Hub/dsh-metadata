# Net ecosystem carbon dioxide (CO 2 ) exchange and meteorological observations collected at peatland ecosystems across Wales, Scotland and England, 2008 to 2020

- Scope
  - Time series of land-surface to atmosphere net ecosystem CO2 exchange (NEE) and supporting micrometeorological observations from thirteen peatland eddy covariance (EC) flux sites across Wales, Scotland and England.
  - Covers 2008–2020 with sites active at different times; dataset represents a subset of site measurements; full variable range is available via Environmental Data Centre (EIDC) records or by contacting authors.

- Study sites and coverage
  - Includes semi-natural and managed peatlands, ranging from upland blanket bogs to lowland fens and agricultural peatlands (grasslands and croplands).
  - Example sites: Crosslochs, Conwy, Moor House, Auchencorth Moss, Cairngorms, Anglesey 1 & 2, Wicken Fen, Bakers Fen, Tadham Moor, Redmere 1 & 2, Rosedene.
  - Precise site coordinates are not provided in the dataset for security and can be obtained from authors.

- Data collection and instrumentation
  - Method: automated eddy covariance flux measurements above the plant canopy.
  - Temporal resolution: raw data at 20 Hz; fluxes computed as 30-minute averages.
  - Micrometeorology: air temperature (TA), relative humidity (RH), vapour pressure deficit (VPD), incoming shortwave radiation (SWIN).
  - Instrumentation details (per site) include height (Zm), datalogger, sonic anemometer, IR gas analyzers, and related sensors (specific models vary by site).

- Data processing and quality control
  - Flux calculation: using EddyPRO software; applies QC, coordinate rotation, high/low-frequency attenuation corrections, humidity-related sensible heat corrections, and density corrections for CO2 and latent heat fluxes.
  - Sign convention: positive NEE = CO2 source to atmosphere; negative NEE = CO2 uptake by ecosystem.
  - Quality control: performed by data providers; removal of outliers, unfavourable conditions, physically implausible values, and limited fetch issues.
  - Representativeness: footprint analysis (ART Footprint Tool) ensures >80% of flux originates within target ecosystem; data plots used for final quality checks.

- Gap filling and flux partitioning
  - Gaps in NEE (and latent heat) filled with Marginal Distribution Sampling (MDS) via REddyProc in R.
  - Longer gaps at Crosslochs filled with a generalized additive model.
  - Daily NEE and uncertainties are gap-filled; NEE uncertainties provided (2 SD).

- Biomass fluxes for agricultural peatlands
  - Table summarises biomass imports/exports for grasslands and croplands (e.g., hay, lettuce, maize, sugar beet, potato) with fluxes in g C m^-2, derived from direct measurements or farm records.
  - Illustrative examples show yearly fluxes and crop-specific uptake/export patterns.

- Data structure and access
  - Data delivered as thirteen site-specific CSV files; each contains complete time series for the site within its start/end dates.
  - Missing records denoted by -9999.
  - Variables included (with units): DateTime (dd/mm/yyyy HH:MM), NEE (g CO2 m^-2 day^-1), NEEunc (g CO2 m^-2 day^-1), TA (°C), VPD (hPa), SWIN (W m^-2), among others (see Table 3 for full list and units).

- Acknowledgments and references
  - Funded by UK Defra (SP1210, SP1218) and UK Natural Environment Research Council programs, Scottish Government, NRW, and others.
  - Dataset tools and references include EddyPRO (Fratini & Mauder), REddyProc, footprint modeling work, and related peatland flux studies.

- Practical relevance for analysts
  - Enables cross-site comparison of CO2 fluxes, energy and water exchange, and responses to management practices and hydrology across UK peatlands.
  - Supports investigations into long-term trends, drivers of inter-annual variability, and the influence of water table and land-use changes on greenhouse gas fluxes.
  - Provides a robust framework for data quality assurance, gap filling, and flux partitioning in complex, multi-site peatland landscapes.