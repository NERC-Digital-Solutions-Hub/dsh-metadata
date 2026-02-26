# Net ecosystem carbon dioxide (CO 2 ) exchange and meteorological observations collected at peatland ecosystems across Wales, Scotland and England, 2008 to 2020

## Overview
- Time series observations of net ecosystem CO2 exchange (NEE) and supporting micrometeorological data
- Collected at thirteen peatland eddy covariance (EC) flux sites across Wales, Scotland and England
- Sites were active at different timescales from 2008 to 2020
- Dataset provides a subset of variables per site; full variable range accessible via Environmental Data Centre (EIDC) records or by contacting the authors

## Study sites
- Flux observations from semi-natural and managed peatlands across the UK
- Site types include blanket bogs and valley fens, and peatlands managed as agricultural grasslands and croplands
- Location map reference: Figure 1
- Site descriptions include start and end dates (Table 1) and general site characteristics
- Coordinates are not included in the data package for security reasons; can be obtained by contacting the authors

## Sampling regime
- Automated flux and meteorological measurements conducted at all sites
- Coverage spans the overall period 2008–2020

## Data acquisition
- Turbulent CO2 fluxes measured above the canopy with eddy covariance systems
- Data streams and sampling details:
  - Vertical velocity components, sonic temperature, water vapour density, and CO2 density at 20 Hz
  - Air temperature (TA) and relative humidity (RH) at 2.0 m above the surface
  - Incoming shortwave radiation (SWIN) above the canopy
- Instrumentation specifics are provided per site in Table 2 (sensor heights, dataloggers, sensors)

## Flux data processing
- Fluxes computed from raw EC data using EddyPRO software
- Averaging interval: 30 minutes
- Processing steps include:
  - Quality control of 20 Hz data
  - Angle-of-attack correction for sonic anemometers
  - Coordinate rotation to align with local terrain
  - Corrections for high/low-frequency co-spectral attenuation
  - Humidity effects on sensible heat flux; density correction for CO2 fluxes
- NEE sign convention: positive when the site is a CO2 source to the atmosphere; negative indicates uptake

## Quality Control
- Per-site quality control by data providers
- QC procedures: removal of statistical outliers, exclusion during periods of high humidity (open-path IRGAs), removal during unfavourable conditions, and exclusion of physically implausible or low-turbulence periods
- For cropland-like sites, footprint representativeness assessed with the ART Footprint Tool; fluxes considered representative if >80% originate within the target ecosystem
- Weekly plotting of flux and ancillary observations to identify and remove clearly erroneous values

## Data gap-filling and flux partitioning
- Data gaps in EC fluxes (LE, H) filled using Marginal Distribution Sampling (Reichstein et al., 2005) via REddyProc in R
- Longer gaps at Crosslochs site filled with a generalized additive model (Levy & Gray, 2015)

## Biomass fluxes for agricultural peatland sites
- Table 3 summarizes biomass imports and exports for grassland and cropland sites
- Positive fluxes represent exports (harvests); negative fluxes represent imports (seeds, plugs, etc.)
- Site- and year-specific examples include Tadham Moor (hay), Redmere farms (crops), Rosedene (lettuce, sugar beet, celery, etc.), with multiple entries across years

## Details of data structure
- Time series data are provided as separate CSV files for each of the thirteen peatland sites
- Each file contains the site-specific time series from the declared start to end dates (Table 1)
- Missing records are denoted by -9999

## Nature and units of recorded values
- Key variables and units included (from Table 3 and accompanying descriptions):
  - DateTime: end of flux observation period (dd/mm/yyyy HH:MM)
  - NEE: daily net ecosystem CO2 exchange; units g CO2 m^-2 day^-1; gap-filled
  - NEEunc: uncertainty of daily gap-filled NEE; units g CO2 m^-2 day^-1
  - TA: air temperature at 2.0 m; °C
  - VPD: vapour pressure deficit; hPa
  - SWIN: incoming shortwave radiation; W m^-2

## Access and data use notes for GIS integration
- Spatial coordinates: not included in the public dataset; can be obtained by contacting the authors
- Full variable set and metadata accessible via Environmental Data Centre (EIDC) records or by authors
- Data formats: time-series CSV files per site; missing data encoded as -9999
- Temporal coverage: 2008–2020 with varying site activity periods
- Useful for GIS applications such as time-enabled visualization of CO2 fluxes, site-based comparisons, and integration with meteorological layers

## Acknowledgments
- Funded by Defra and UK Research Councils, with contributions from multiple projects and partners
- Data processing and site-specific support acknowledged in the dataset documentation