# Net ecosystem carbon dioxide (CO 2 ) exchange and meteorological observations collected at peatland ecosystems across Wales, Scotland and England, 2008 to 2020

- Dataset scope
  - Time series of net ecosystem CO2 exchange (NEE) and supporting micrometeorological observations from thirteen peatland eddy covariance flux sites across Wales, Scotland, and England.
  - Sites were active at different times between 2008 and 2020; the dataset in this document includes a subset of variables measured at each site and is provided as supplementary material to Evans et al. (in press).
  - The full range of variables can be accessed via Environmental Data Centre (EIDC) records and/or by contacting the authors.

- Study sites
  - thirteen peatland flux observation sites with a mix of semi-natural and managed peatlands (e.g., blanket bogs, valley fens, croplands, grasslands).
  - Examples include Crosslochs, Conwy, Moor House, Auchencorth Moss, Cairngorms, Anglesey 1 & 2, Wicken Fen, Bakers Fen, Tadham Moor, Redmere 1 & 2, and Rosedene.
  - Site coordinates are not provided in this document for security reasons; coordinates can be obtained by contacting the authors.

- Sampling regime and data collection
  - Automated flux and meteorological measurements at each site, spanning 2008–2020.
  - Above-canopy turbulent fluxes measured with eddy covariance (EC) systems at 20 Hz; 30-minute flux averaging.
  - Supporting micrometeorological sensors include air temperature, relative humidity, wind, radiation, and CO2 density measurements.
  - Key variables measured: NEE, wind components, sonic temperature, CO2 density, air temperature, relative humidity, incoming shortwave radiation, among others (site-specific instrumentation summarized in Table 2).

- Data processing and quality control
  - Fluxes calculated with EddyPRO® using standard processing steps and corrections (QC of raw data, angle-of-attack corrections, coordinate rotation, spectral corrections, density corrections for sensible and latent heat and CO2 fluxes).
  - Sign convention: positive NEE denotes CO2 source to the atmosphere; negative NEE denotes uptake by the ecosystem.
  - Quality control applied by providers, including removal of outliers, exclusion during high humidity or adverse conditions (open-path IRGAs), implausible values, and low turbulence periods.
  - Footprint representativeness assessed where appropriate; fluxes considered representative if >80% originated within the target ecosystem.
  - Weekly checks of flux and ancillary data to identify and remove clearly erroneous values.

- Data gap-filling and flux partitioning
  - Gaps in EC data (LE, H) filled using Marginal Distribution Sampling with the REddyProc package in R.
  - Longer gaps at Crosslochs filled with a generalized additive model (Levy & Gray, 2015).

- Biomass fluxes for agricultural peatlands
  - Table 3 provides imports/exports of biomass for grassland and cropland peatlands (positive exports, negative imports).
  - Examples include Tadham Moor (hay), Redmere Farm 1 & 2 (various crops), and Rosedene Farm (lettuce, celery, beet, etc.) across multiple years.
  - Biomass fluxes expressed in g C m-2.

- Data structure and units
  - Time series data delivered as separate CSV files for each of the thirteen peatland sites.
  - Data cover complete time series for each site within the specified start/end dates; missing records denoted as -9999.
  - Variables and units (examples): DateTime (dd/mm/yyyy HH:MM); NEE (g CO2 m-2 day-1); NEEunc (g CO2 m-2 day-1); TA (°C); VPD (hPa); SWIN (W m-2).
  - The full variable descriptions and units are detailed in the dataset documentation derived from LI-COR and Reichstein et al. (2016) conventions.

- Access, metadata and limitations
  - Full range of variables and accompanying metadata are available via the Environmental Data Centre (EIDC) or by contacting the dataset authors.
  - Site coordinates are withheld in this document but can be provided on request.
  - The dataset is provided as supplementary material to Evans et al. (in press), with broader project context and data provenance described in the referenced publications.

- Acknowledgments and references
  - Funded by Defra (SP1210, SP1218) and supported by NERC, Scottish Government, NRW, and UK-SCAPE/UKCEH programs.
  - Methodological and analytical references include EddyPRO processing, QC standards, footprint analyses, gap-filling methods (REddyProc), and related peatland GHG flux studies.