# Net ecosystem carbon dioxide (CO2) exchange and meteorological observations collected at peatland ecosystems across Wales, Scotland and England, 2008 to 2020

## Overview and purpose
- Time series observations of net ecosystem CO2 exchange (NEE) and supporting micrometeorological data from thirteen peatland eddy covariance (EC) flux sites across Wales, Scotland and England.
- Includes a subset of variables measured at each site; full variable set available via Environmental Data Centre (EIDC) records or by contacting the authors.
- Data are supplementary material to Evans et al. (in press) and span 2008–2020 with sites activated at differing times.

## Study sites and type
- Flux observations from semi-natural and managed peatlands, globally varied in management and use.
- Site types include blanket bogs and valley fens; some peatlands are heavily managed as agricultural grasslands or croplands.
- Thirteen sites (examples): Crosslochs, Conwy, Moor House, Auchencorth Moss, Cairngorms, Anglesey 1, Anglesey 2, Wicken Fen, Bakers Fen, Tadham Moor, Redmere 1, Redmere 2, Rosedene.
- Site coordinates are not provided in this document for security reasons; coordinates can be obtained by contacting the authors.
- Start and end dates for each site are listed; overall 2008–2020 sampling regime with varying site durations.

## Data acquisition and instrumentation
- Automated turbulent flux and meteorological measurements above the plant canopy using eddy covariance (EC) systems.
- Sampling at 20 Hz for raw EC data (three wind components, sonic temperature, density of water vapor and CO2).
- Ancillary meteorological data: air temperature (TA) and relative humidity (RH) at 2.0 m; incoming shortwave radiation (SWIN) above the canopy.
- Instrumentation details summarized per site (e.g., tower height, datalogger, sensors) in Table 2 of the document.

## Data processing, quality control, and flux estimation
- Fluxes calculated from raw EC data with EddyPRO processing software; 30-minute averaging.
- Processing steps include:
  - Quality control of 20 Hz data.
  - Angle-of-attack correction for certain sonic anemometers.
  - Coordinate rotation to align data to local terrain.
  - Corrections for high/low-frequency co-spectral attenuation, humidity effects on sensible heat, and density corrections for CO2 and latent heat fluxes.
- NEE sign convention: positive NEE = CO2 release to the atmosphere; negative NEE = uptake.
- Quality control (QC) performed by data providers:
  - Removal of statistical outliers, periods of high humidity (for open-path IRGAs), unfavourable conditions, physically implausible values, and low turbulence periods.
  - Footprint analysis to ensure representativeness (≥80% of flux originating within target ecosystem) for cropland sites.
  - Weekly visual checks of flux and ancillary data to remove clearly erroneous values.

## Gap filling and flux partitioning
- Gaps in EC data (NEE, LE, H) filled using Marginal Distribution Sampling via REddyProc (R) package.
- Crosslochs site gaps filled with a generalized additive model approach.
- Flux partitioning and uncertainty quantification follow standard REddyProc methodologies.

## Biomass fluxes for agricultural peatlands
- Biomass imports/exports for grassland and cropland sites summarized (Table 3).
- Positive values indicate exports (harvest, etc.); negative values indicate imports (seeds, crops).
- Example data entries include Tadham Moor, Redmere and Rosedene sites across multiple years and crops (e.g., hay, lettuce, maize, sugar beet, potato) with flux values provided in g C m-2.
- Data cover site-specific biomass transactions and may be useful for biomass balance analyses of managed peatlands.

## Data structure, contents, and units
- Time series are provided as separate CSV files for each of the thirteen sites.
- Each file contains complete time series for the site, with missing records denoted as -9999.
- Variables and units (as per Table 3):
  - DateTime: dd/mm/yyyy HH:MM
  - NEE: g CO2 m^-2 day^-1 (daily, gap-filled; positive = emission, negative = uptake)
  - NEEunc: g CO2 m^-2 day^-1 (uncertainty; 2 SD)
  - TA: °C (air temperature at 2.0 m)
  - VPD: hPa (vapour pressure deficit)
  - SWIN: W m^-2 (incoming shortwave radiation)
  - Other site-specific micrometeorological variables and flux components are described in the data documentation and associated tables.

## Access, usage, and metadata
- Primary dataset: UK_Peatlands_NEE_Flux_Dataset.zip.
- Full range of variables available via Environmental Data Centre (EIDC) or by contacting the study authors.
- Data processing and QC workflows are documented to support reproducibility and reuse in data products, dashboards, and analyses.

## Acknowledgments and references
- Funded by Defra (SP1210, SP1218) with additional support from UK Natural Environment Research Council (SEFLOS NE/P014097/1; UKSCAPE) and other agencies.
- Data processing support from NERC awards and institutional partners; site-level data acquisition supported by peatland and governmental programs.
- Key references include methodological papers on eddy covariance processing, QC, footprint analyses, and REddyProc gap-filling tools (e.g., Reichstein et al., Mauder et al., Moncrieff et al., Levy & Gray, Neftel et al., etc.), and project-specific publications linked in the document.