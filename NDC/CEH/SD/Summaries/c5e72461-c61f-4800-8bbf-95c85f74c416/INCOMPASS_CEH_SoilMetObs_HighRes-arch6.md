# High temporal resolution meteorology and soil physics observations from INCOMPASS land surface stations in India, 2016 to 2018

## Overview
- Time-series data of meteorological and soil physics variables at 1-minute resolution from three INCOMPASS Land Surface Stations in India (Berambadi, Dharwad, Kanpur).
- Observation period: 2016-01-01 00:01 to 2019-01-01 00:00 (Kanpur ends 2018-08-28 06:23).
- Stations located in: Berambadi (agricultural land, Southern Karnataka), Dharwad (University of Agricultural Sciences, northern Karnataka), Kanpur (semi-natural grassland at IIT Kanpur, Uttar Pradesh).
- Purpose: enable examination of high-temporal dynamics of surface energy fluxes, meteorology, and soil physics; suitable for model validation and data product development.

## Study sites and site characteristics
- Berambadi, Southern Karnataka
  - Location: 11.760633°N, 76.585361°E; altitude 873 m
  - Climate: Aw (tropical monsoon), ~600 mm annual rainfall
  - Land use: Mixed agriculture; Alfisol soils
- Dharwad, Northern Karnataka
  - Location: 15.498393°N, 74.985730°E; altitude 692 m
  - Climate: Aw (tropical savannah), ~885 mm rainfall
  - Land use: Agriculture; Vertisol soils
- Kanpur, Uttar Pradesh
  - Location: 26.509072°N, 80.223765°E; altitude 129 m
  - Climate: Csa (humid subtropical), ~820 mm rainfall
  - Land use: Semi-natural grassland; Fluvisol soils

## Sampling regime
- Measurements at Berambadi and Dharwad: 2016-01-01 to 2019-01-01.
- Measurements at Kanpur: 2016-01-01 to 2018-08-28 06:23.
- Instrumentation identical across sites; 1-minute logging with 0.1 Hz sensor scans; precipitation totals aggregated.
- Close collaboration with farm/academic sites for data collection and access.

## Measurements and instrumentation
- Meteorological observations (all at 10 m mast):
  - Barometric pressure (PA, kPa)
  - Air temperature (Ta, °C) and relative humidity (RH, %)
  - Net radiation and components: Rnet, SWin, SWout, LWin, LWout (W m^-2)
  - Wind speed (WS, m s^-1) and wind direction (WD, degrees, from north)
  - Precipitation (mm min^-1)
- Soil physics observations (duplicated at two locations per site):
  - Soil heat flux (G1, G2, W m^-2) at 0.03 m depth
  - Soil temperature (Tsoil) at 0.05 m and 0.15 m depths
  - Soil volumetric water content (VWC) at 0.05 m and 0.15 m
- Instrument suite:
  - LI-7500A (barometric pressure), HMP155 (Ta, RH) in TS-100 shield
  - NR01 Net Radiometer (Rnet, components)
  - WindSonic (WS, WD)
  - SBS314 rain gauge (precipitation)
  - G, VWC, and Tsoil sensors: HFP01-SC, ACC-SEN-SDI
- Data are 1-minute means; precipitation sums are per-minute totals.

## Data structure and quality control
- Data delivered as separate CSV files per site.
- Each file contains time-stamped observations with columns defined in the data description; timestamps are end-of-interval (Indian Standard Time, UTC+5:30).
- Missing data denoted by -9999.
- Quality control:
  - Basic range checks and visual spike/dropout checks for meteorology.
  - Cross-checks for soil fluxes, soil temperature, and soil moisture against corresponding depths and with rainfall data.
  - Large changes in soil moisture cross-checked with rainfall and flooding indicators (notably at Kanpur).
  - Clearly erroneous data removed from time series.

## Variables and units (high-level)
- Meteorology (per minute):
  - Pa (kPa), Ta (°C), RH (%)
  - SWin, SWout, LWin, LWout, Rnet (W m^-2)
  - Precipitation (mm min^-1)
  - WS (m s^-1), WD (degrees)
- Soil physics (per site/depth):
  - G1, G2 (soil heat flux, W m^-2)
  - Tsoil at 0.05 m and 0.15 m (°C)
  - VWC at 0.05 m and 0.15 m (%, two depths, two locations)

## Access, format, and usage notes
- Data are provided as complete time series for each site, with end timestamps specified above.
- -9999 indicates missing data.
- Time zone: Indian Standard Time (UTC+5:30).
- Data suitable for cross-site comparisons, anomaly detection, and development of data products (e.g., dashboards, time-series analyses, model validation).

## Context, acknowledgments, and references
- Part of the INCOMPASS project (Interaction of Convective Organization and Monsoon Precipitation, Atmosphere, Surface and Sea).
- UK-India collaboration; funding from Natural Environment Research Council (NERC) and India MoES, with additional project support.
- Acknowledges site owners and collaborators from IISc, UAS Dharwad, IIT Kanpur, and related institutions.
- References include Chakraborty et al. (2019) on surface energy flux biases, Climate-Data.org climate data, Köppen-Geiger climate classification, and related resources.