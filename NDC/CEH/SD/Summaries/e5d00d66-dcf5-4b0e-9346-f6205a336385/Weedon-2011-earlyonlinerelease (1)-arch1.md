# WATCH Forcing Data

## Overview
- A long-term meteorological forcing dataset (WFD) designed for land surface and hydrological models across the 20th century.
- Provides diurnally resolved forcing on a half-degree grid, suitable for driving models globally and basin-scale analyses.

## Data structure and forcing variables
- Global half-degree grid (CRU land–sea mask).
- Forcing variables include:
  - Wind speed at 10 m, temperature at 2 m, surface pressure, specific humidity at 2 m
  - Downward longwave and shortwave radiation
  - Rainfall rate, snowfall rate
- Temporal resolution:
  - 3-hourly data for precipitation components
  - 6-hourly data for wind, temperature, pressure, humidity, and longwave
- Precipitation handling:
  - Preserves ERA-40 rain/snow proportion per grid box
  - Wet-day corrections to align with CRU GPCC totals
- Bias corrections and adjustments:
  - Temperature and related variables bias-corrected using CRU observations
  - Relative humidity derived from corrected variables
  - Shortwave radiation corrected for cloud cover and tropospheric aerosols
  - Longwave radiation adjusted with ERA-40 basis; no separate SRB bias correction
  - Aerosol and cloud corrections incorporated; corrections maintain spatial coherence
- Pre-1958 data (1901–1957):
  - Years drawn randomly from ERA-40 to match 1958–2001 statistics
  - Similar processing and corrections; interannual variability pre-1958 is approximate due to data limitations

## PET_rc and PET_PT estimation
- PET_rc: Penman–Monteith reference evapotranspiration for a well-watered grass reference crop
  - Uses aerodynamic and surface resistances tied to WFD wind data
- PET_PT: Priestley–Taylor PET using available energy approximated by net radiation
- Comparisons illustrate how PET definitions respond to drivers such as net radiation, VPD, wind, and temperature

## Global and regional findings
- PET_rc trends (1958–2001): global PET_rc declines modestly with high interannual variability; regional basins show diverse behavior.
- Pre-1958 (1901–1957): no robust global PET_rc trend; regional patterns are more variable due to data limitations.
- Precipitation:
  - No robust global trend (1958–2001); regional changes exist, with some basins showing aridity trends when PET_rc is high
- Drivers and interactions:
  - PET_rc is influenced by VPD, net radiation, and wind; shifts in these drivers can offset each other, yielding complex regional signals
- Validation against FluxNet and tower data:
  - Temperature and radiation show strong correlations and good diurnal representation
  - Precipitation, especially sub-daily structure, shows weaker agreement in some regions
  - Wind shows variable agreement; topography and land-cover differences affect comparisons
- Limitations and caveats:
  - Early-period data (1901–1957) rely on random year selection and sparser networks, potentially dampening decadal signals
  - Pre-1958 aerosol, cloud, and wind corrections carry uncertainties
  - Sub-grid orography and land-cover differences can bias comparisons to local observations

## Access, usage, and caveats
- WFD is designed for consistent, comparable forcing across large basins and global land areas.
- Users should consider uncertainties in early-century data, limited short-timescale precipitation representation, and residual biases in aerosol, cloud, and wind corrections.
- Explicit documentation of uncertainties and trend assessments supports hydroclimate risk analyses and model intercomparisons.

## Appendix notes

### Appendix: ERA-40 basis years (1901–1957)
- The order of ERA-40 basis years as used in the WATCH Forcing Data 1901–1957
- WFD, 1 = ERA-40; WFD, 2 = WFD; WFD, 3 = ERA-40; WFD, 4 = WFD; WFD, 5 = ERA-40
- Each year (1901–1957) is assigned to basis years with specific mappings (e.g., 1901 = 1st basis year = 1974; 1901, 2 = 1920; etc.)
- This table documents the sequencing used to construct the 1901–1957 forcing basis from ERA-40 years

### Appendix: Basin-level statistics (examples)
- The document contains detailed basin-by-basin statistics for:
  - PET_rc (mm/yr) and PET_PT (mm/yr)
  - Net radiation (W/m^2)
  - VPD (kPa)
  - Wind (m/s)
  - Rainfall and Snowfall (mm/yr)
  - Precipitation (mm/yr)
- Time intervals analyzed include 1901–1957, 1958–2001, and 1979–2001, with slopes, averages, and significance (Adjusted Slope P) values
- Basins covered include Orange, Murray-Darling, Lena, Ganges–Brahmaputra, and others, illustrating regional variability in climate drivers and PET responses

## Access and references
- WFD documentation and data release: WATCH Technical Report 22 and related resources at www.eu-watch.org
- Key methodological references: ERA-40 reanalysis, CRU observations, GPCC precipitation, GPCC cloud corrections, and FluxNet validations