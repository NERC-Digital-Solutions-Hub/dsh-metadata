# Meteorological and atmospheric dust data from Kangerlussuaq, southwest Greenland, 2017-2019

## Overview
- A multi-dataset collection from Kangerlussuaq, southwest Greenland (2017–2019) covering atmospheric dust, weather conditions, wind, and dust deposition.
- Datasets span two monitoring sites (Ridge and SS85) and five deposition locations, plus particle-size data for deposited dust.
- Instruments include TSI DustTrak DRX and various meteorological sensors; data include time series, seasonal deposition measurements, and particle-size distributions.
- Data are provided as CSV files with defined structures, units, and operational periods; notable data gaps due to power/equipment issues.

## Datasets and key details

- DUSTY_DustTrak.csv
  - Purpose: Atmospheric dust concentrations at Ridge and SS85.
  - Instrument: TSI DustTrak DRX Environmental Monitor (inlet height ≈ 2.5 m AGL).
  - Operational dates: Ridge (2018-04-19 to 2018-10-03; 2019-04-13 to 2019-08-22); SS85 (2018-04-21 to 2018-10-06; 2019-04-21 to 2019-08-16).
  - Sampling: Average dust concentration per 1 minute, reported every 5 minutes.
  - Missing data: 63.9%–99.9% missing per sampling period due to power auto-zero and equipment issues.
  - Units: mg m^-3.
  - Structure: A – Date/Time; B – Site; C–G – PM1, PM2.5, RESP, PM10, Total.

- DUSTY_Weather_Station_Temperature_and_Humidity_Data.csv
  - Purpose: Air temperature, humidity, and related metrics at Ridge and SS85.
  - Instrument: Omega OMYL-RH20 (~1 m AGL).
  - Operational dates: Ridge (2018-04-19 to 2018-10-07; 2019-04-11 to 2019-08-22); SS85 (2018-04-21 to 2018-10-07; 2019-04-21 to 2019-08-16).
  - Sampling: 1 reading every 10 minutes.
  - Missing data: Completeness 98.4%–100% per sampling period; occasional gaps due to power/equipment issues.
  - Units: Temperature (°C); Relative humidity (%); Absolute humidity (g m^-3); Dew Point (°C).
  - Structure: A – Date/Time; B – Site; C – Temperature; D – Relative humidity; E – Absolute humidity; F – Dew Point.

- DUSTY_Weather_Station_Wind_Data.csv
  - Purpose: Wind speed and direction at Ridge and SS85.
  - Instrument: RMYoung 5013 sensor (~2.5 m AGL).
  - Operational dates: Ridge (2018-04-15 to 2018-10-06; 2019-04-11 to 2019-08-22); SS85 (2018-04-18 to 2018-10-07; 2019-04-11 to 2019-08-16).
  - Sampling: 1 reading every 5 minutes.
  - Missing data: 66.4%–99.9% missing per sampling period due to power/equipment issues.
  - Units: Mean wind speed (m s^-1); Max wind speed (m s^-1); Min wind speed (m s^-1); Wind direction (degrees).
  - Structure: A – Date/Time; B – Site; C – Mean wind speed; D – Max wind speed; E – Min wind speed; F – Wind direction.

- HDT_Deposition_Data.csv
  - Purpose: Dust deposition measurements at five locations.
  - Locations: SS906, Ridge, SS17b, SS1590, SS85.
  - Instrument: Hall Deposition Trap (trap head height 1.5–1.8 m AGL).
  - Operational dates: Sp2017 (23 Apr 2017–20 Jun 2017); Su2017 (21 Jun 2017–12 Aug 2017); FaWi1718 (12 Aug 2017–13 Apr 2018); Sp2018 (14 Apr 2018–16 Jun 2018); Su2018 (17 Jun 2018–13 Aug 2018); FaWi1819 (14 Aug 2018–13 Apr 2019).
  - Sampling frequency: At end of each season (seasonal aggregation).
  - Retrieval and measurement protocol: Sediment collected, dried, weighed, ashed, and LOI used to estimate minerogenic dust mass; final areal deposition calculated using trap geometry and collection period.
  - Missing data: 4–5 traps per location; “n/d” indicates no data due to trap damage or loss.
  - Units: g m^-2 day^-1.
  - Structure: A – Location; B – Trap number (1–5); C–H – Seasonal data columns (Sp2017, Su2017, FaWi1718, Sp2018, Su2018, FaWi1819).

- Particle-size data (deposited dust)
  - Purpose: Particle size distributions for dust trapped at five locations.
  - Instrument: Beckman Coulter LS 230 laser sizer (0.375–2000 µm; 93 size classes).
  - Operational notes: If total dust mass is low, samples from all HDTs at a location are bulked to produce an average size distribution.
  - Units: Areal dust deposition per trap; size distribution in µm.
  - Structure: Size (µm); Columns for trap numbers (HDT1–HDT4/5) across locations.

- Data files and location mapping for deposition dataset
  - PSA906_DUST_HDT.csv (SS906)
  - PSAR_DUST_HDT.csv (Ridge)
  - PSA17b_DUST_HDT.csv (SS17b)
  - PSA1590_DUST.csv (SS1590)
  - PSA85_DUST_HDT.csv (SS85)

## Data structure and formats
- All data are provided as CSV (comma-separated values) files; labeled with clear column definitions.
- Key data columns across datasets include Date/Time, Site (Ridge or SS85), and measurement-specific variables (dust fractions, temperature, humidity, wind metrics, deposition, or particle-size data).

## Data quality, gaps, and caveats
- Substantial missing data in air-dust concentration (63.9%–99.9% per period) and wind data (66.4%–99.9%), largely due to power outages and equipment malfunctions.
- Weather data show high completeness (roughly 98.4%–100%), with occasional gaps from similar issues.
- Deposition and particle-size datasets are seasonal aggregates with occasional missing traps; data quality dependent on trap integrity.

## Spatial and temporal coverage
- Timeframe: 2017–2019 for all datasets.
- Locations: Ridge and SS85 (dust and weather data); five deposition sites (SS906, Ridge, SS17b, SS1590, SS85); particle-size data correspond to the same five locations.
- Seasonal deposition data are reported per season across multiple years.

## Potential data products and uses
- Time-series dashboards comparing dust concentrations (PM1/PM2.5/PM10/Respirable) with local meteorology (temperature, humidity, wind) by site.
- Cross-site comparison of deposition rates and seasonal patterns.
- Particle-size distribution profiles by location and season to assess dust transport and source characteristics.
- Data quality checks and imputation strategies to handle gaps for modeling and visualization.
- Data fusion opportunities: align DustTrak measurements with wind vectors to study transport and dispersion; correlate deposition with seasonal meteorology.

## Access and data organization notes
- Data are organized by dataset, with explicit file names linking to sites and measurements.
- Particle-size data are provided both as deposition totals per location and as size-distribution data, enabling multivariate analyses of deposition composition.
- Documentation includes detailed descriptions of instruments, operational periods, sampling frequencies, and measurement protocols to support data cleaning and integration for end users.