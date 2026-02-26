# High temporal resolution meteorology and soil physics observations from INCOMPASS land surface stations in India, 2016 to 2018

## Overview
- Dataset of one-minute time series for meteorological and soil physics variables.
- Collected at three INCOMPASS Land Surface Stations in India between 2016-01-01 00:01 and 2019-01-01 00:00 (Kanpur data up to 2018-08-28 06:23).
- Sites: Berambadi (Southern Karnataka), Dharwad (Northern Karnataka), and Kanpur (Uttar Pradesh).
- Purpose: supporting analyses of convective organization, monsoon precipitation, atmosphere–surface interactions, and energy fluxes, with standardized formatting for cross-study scrutiny.

## Study Sites
- Berambadi, Southern Karnataka
  - Location: 11.760633°N, 76.585361°E, 873 m amsl; semi-arid tropical monsoon Aw climate; Alfisol soil.
  - Land use: Mixed agriculture; near Western Ghats foothills.
  - Mean annual temp ~24.4°C; rainfall ~600 mm.
- Dharwad, Northern Karnataka
  - Location: 15.498393°N, 74.985730°E, 692 m amsl; tropical savannah Aw climate; Vertisol soil.
  - Land use: Agricultural; campus site at University of Agricultural Sciences (UAS) Dharwad.
  - Mean annual temp ~24.3°C; rainfall ~885 mm.
- Kanpur, Uttar Pradesh
  - Location: 26.509072°N, 80.223765°E, 129 m amsl; humid subtropical Csa climate; Fluvisol soil.
  - Land use: Semi-natural grassland; periodic flooding risk from nearby canal.
  - Mean annual temp ~25.6°C; rainfall ~820 mm.

## Data Collection and Instrumentation
- Identical instrumentation at all three stations.
- Meteorological sensors at 10 m mast; soil sensors at two depths (0.05 m and 0.15 m) at two locations per site.
- Instruments include: barometric pressure, air temperature, relative humidity, net radiation and components (SWin, SWout, LWin, LWout, Rnet), wind speed/direction, and precipitation.
- Soil measurements: soil heat flux (0.03 m), volumetric water content (VWC) at 0.05 and 0.15 m, soil temperature at 0.05 and 0.15 m.
- Data logged at 0.1 Hz and aggregated to one-minute means; precipitation summed per minute.
- Sensor brands: LI-7500A, HMP155 in aspirated shield, NR01 Net Radiometer, WindSonic, SBS314 rain gauge; soil sensors include HFP01-SC and ACC-SEN-SDI.

## Sampling Regime and Temporal Coverage
- Berambadi and Dharwad: continuous automated measurements from 2016-01-01 to 2019-01-01.
- Kanpur: continuous measurements from 2016-01-01 to 2018-08-28 06:23.
- Data quality checks implemented during collection and QC processes.

## Meteorological Observations
- Variables recorded per time point (units):
  - Pa (kPa): Barometric pressure
  - Ta (°C): Air temperature
  - RH (%): Relative humidity
  - SWin, SWout (W m^-2): Incoming/outgoing shortwave radiation
  - LWin, LWout (W m^-2): Incoming/outgoing longwave radiation
  - Rnet (W m^-2): Net radiation
  - Precipitation (mm min^-1): Total precipitation per minute
  - WS (m s^-1): Wind speed at 10 m
  - WD (degrees): Wind direction from north
- Data captured at 0.1 Hz and aggregated to 1-minute means; two locations for redundancy.

## Soil Physics Observations
- Depths: 0.05 m and 0.15 m, at two locations per site.
- Measurements include:
  - G1, G2 (W m^-2): Soil heat flux at 0.03 m depth
  - Tsoil_0.05_1, Tsoil_0.15_1, Tsoil_0.05_2, Tsoil_0.15_2 (°C): Soil temperatures
  - VWC_0.05_1 %, VWC2_0.15_1 %, VWC1_0.05_2 %, VWC2_0.15_2 %: Soil volumetric water content
- Observations co-located with radiometer sensors; data also at 0.1 Hz, summarized to one-minute means.

## Data Quality Control
- QC steps include range checks, spike/dropout screening, and cross-checks between paired soil observations.
- Large soil moisture changes validated against rainfall and documented flooding (Kanpur).
- Clearly erroneous data removed from time series.

## Data Structure and Format
- Data provided as separate CSV files for each station.
- Each file contains a complete time series from start to end dates listed above.
- Time stamps use Indian Standard Time (UTC+5:30); missing data encoded as -9999.
- Columns align with Table 2: DateTime, Pa, Ta, RH, SWin, SWout, LWin, LWout, Rnet, Precipitation, WS, WD, G1, G2, Tsoil_0.05_1, Tsoil_0.15_1, Tsoil_0.05_2, Tsoil_0.15_2, VWC_0.05_1, VWC2_0.15_1, VWC1_0.05_2, VWC2_0.15_2.

## Variables and Units (Summary)
- DateTime: yyyy-mm-dd HH:MM (IST)
- Pa: kPa
- Ta: °C
- RH: %
- SWin/SWout: W m^-2
- LWin/LWout: W m^-2
- Rnet: W m^-2
- Precipitation: mm per minute
- WS: m s^-1
- WD: degrees
- G1/G2: W m^-2
- Tsoil_0.05_1, Tsoil_0.15_1, Tsoil_0.05_2, Tsoil_0.15_2: °C
- VWC_0.05_1, VWC2_0.15_1, VWC1_0.05_2, VWC2_0.15_2: %

## Data Availability and Timeline
- INCOMPASS project funding from UK and India support; additional support for some authors from related programs.
- Data accessible as described in the dataset documentation; suitable for integration with other environmental datasets and time-series analyses.

## Acknowledgments and References
- Acknowledges INCOMPASS project funders, site owners, and collaborators from IISc, UAS Dharwad, IIT Kanpur, CHE, and University of Leeds.
- References include methodological and climate-data sources used for site context and QC considerations.

## Relevance for Environmental Monitoring Analysts
- Provides a high-temporal-resolution, standardized dataset for evaluating surface energy balance, meteorology, and soil moisture dynamics.
- Enables cross-site comparisons and integration with broader monitoring datasets.
- QC-focused, with clear data structure and missing value conventions to support reproducible analyses and policy-relevant environmental health assessments.