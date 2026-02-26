# Net ecosystem carbon dioxide (CO 2 ) exchange and meteorological observations collected at peatland ecosystems across Wales, Scotland and England, 2008 to 2020

- Purpose and scope
  - Time series of land surface–atmosphere net ecosystem CO2 exchange (NEE) and supporting micrometeorological observations.
  - Collected at thirteen peatland eddy covariance (EC) flux sites across Wales, Scotland and England.
  - Time period: 2008–2020; sites active at different timescales within this window.
  - Dataset in the UK_Peatlands_NEE_Flux_Dataset.zip; subset of variables per site; full variable range available via Environmental Data Centre (EIDC) records or by contacting authors.
  - Supplementary material to Evans et al. (in press).

- Study sites and geography
  - Flux observations from semi-natural and managed peatlands, including blanket bogs, valley fens, and croplands/grasslands.
  - Sites: Crosslochs, Conwy, Moor House, Auchencorth Moss, Cairngorms, Anglesey 1, Anglesey 2, Wicken Fen, Bakers Fen, Tadham Moor, Redmere 1, Redmere 2, Rosedene.
  - Start and end dates per site (e.g., Crosslochs 2008–2013; Auchencorth Moss 2012–2019; Tadham Moor 2012–2020; etc.).
  - Site coordinates not supplied in the dataset for security reasons; can be obtained by contacting authors.
  - Figure: map illustrating the peatland EC sites across the UK.

- Data collection and instrumentation
  - Automated flux and meteorological measurements spanning 2008–2020.
  - Eddy covariance (EC) systems used to measure turbulent fluxes of NEE above the canopy.
  - 20 Hz raw data for wind components, sonic temperature, water vapor density, and CO2 density; additional meteorological measurements (TA, RH, SWIN) at specified heights.
  - Site-specific instrumentation details provided (e.g., Zm height, datalogger type, sensors for IRGASON LI-7500/LI-7200, etc.).
  - Supporting data include incoming shortwave radiation (SWIN) and other micrometeorological variables.

- Data processing and formats
  - Fluxes calculated from raw EC data using EddyPRO® with 30-minute averaging.
  - Processing steps include QC of 20 Hz data, angle-of-attack correction, coordinate rotation, co-spectral attenuation corrections, density corrections for heat and moisture, and CO2 flux adjustments.
  - NEE sign convention: positive when the site is a CO2 source to the atmosphere; negative when it is a sink.
  - Data are organized as separate CSV files for each site; end-of-period timestamps included; -9999 denotes missing data.

- Quality control and data quality
  - Quality control performed by data providers; includes removal of outliers, high-humidity periods (for open-path IRGAs), physically implausible fluxes, and periods of low turbulence.
  - Footprint assessment (for croplands) to ensure representativeness; fluxes considered representative if >80% originated within target ecosystem (ART Footprint Tool).
  - Weekly plots used to identify and remove clearly erroneous values.

- Data gap filling and flux partitioning
  - Gaps in EC data (LE, H) filled using Marginal Distribution Sampling (Reichstein et al., 2005) via REddyProc in R.
  - Crosslochs site gap-filled with a generalized additive model (Levy & Gray, 2015).
  - Net ecosystem exchange partitioned into components as part of standard processing approaches.

- Biomass fluxes for agricultural peatlands
  - Table 3 summarizes biomass imports and exports (e.g., harvested crops) for grassland and cropland sites.
  - Data sourced from direct measurements and farm records; includes year, crop, date, and flux values (positive = exports, negative = imports).

- Data structure and access
  - Time series data delivered as CSV files, one per site, with complete time series within documented start/end dates.
  - Missing records denoted by -9999.
  - Extended laboratory and site-level metadata available in associated tables (e.g., Table 2: instrumentation, Table 3: variables and units).

- Variables, units, and dataset notes
  - Key variables include DateTime, NEE (g CO2 m^-2 day^-1), NEEunc, TA (°C), VPD (hPa), SWIN (W m^-2), among others.
  - Variable descriptions and units align with LI-COR conventions and Reichstein et al. processing standards.

- Acknowledgments and funding
  - Funded by UK Department for Environment, Food and Rural Affairs (Defra) SP projects and UK Natural Environment Research Council (NERC) programs, among others.
  - Data processing and acquisition supported by multiple institutions and grants; collaboration with landowners and site managers acknowledged.

- Usage considerations for analysts
  - Suitable for monitoring and evaluating peatland carbon dynamics, greenhouse gas fluxes, and ecosystem health over time.
  - Allows cross-site comparisons after accounting for site-specific start/end times, footprint representativeness, and processing steps.
  - Access to full variable sets and metadata may require contacting authors or the EIDC; coordinates are restricted in the public dataset but can be obtained upon request.
  - Methodological references provide a robust basis for processing, QC, gap-filling, and flux partitioning in eddy covariance analyses.