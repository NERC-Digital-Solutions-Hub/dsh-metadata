# High temporal resolution meteorology and soil physics observations from INCOMPASS land surface stations in India, 2016 to 2018

## Overview
- Time series observations at one-minute resolution from three INCOMPASS Land Surface Stations in India.
- Data collection period: 2016-01-01 00:01 to 2019-01-01 00:00 (Kanpur ends 2018-08-28 06:23).
- Sites: Berambadi (Southern Karnataka, agricultural land), Dharwad (University of Agricultural Sciences Dharwad, agricultural), Kanpur IITK (semi-natural grassland, Uttar Pradesh).
- Purpose: part of the INCOMPASS project investigating interactions between convection, monsoon precipitation, atmosphere, surface, and sea.

## Sites and temporal coverage
- Berambadi: 11.760633°N, 76.585361°E, altitude 873 m; climate Aw; soil Alfisol; mean annual temp ~24.4°C; ~600 mm rainfall.
- Dharwad: 15.498393°N, 74.985730°E, altitude 692 m; climate Aw; soil Vertisol; mean annual temp ~24.3°C; ~885 mm rainfall; agricultural field surrounding flux tower.
- Kanpur: 26.509072°N, 80.223765°E, altitude 129 m; climate Csa; soil Fluvisol; mean annual temp ~25.6°C; ~820 mm rainfall; semi-natural grassland with periodic flooding.

## Sampling regime and instrumentation
- Measurements at Berambadi and Dharwad: 2016-01-01 to 2019-01-01.
- Measurements at Kanpur: 2016-01-01 to 2018-08-28 06:23.
- Instruments (identical across sites):
  - Meteorology: barometric pressure (PA), air temperature (Ta), relative humidity (RH), net radiation (Rnet) with short/longwave components, wind speed (WS) and direction (WD), precipitation.
  - Soil physics: duplicated soil heat flux (G) at 0.03 m, soil water content (VWC) and soil temperature (Tsoil) at 0.05 and 0.15 m depths.
- Data logging: 0.1 Hz sensor scans, then 1-minute means; timestamps in Indian Standard Time (UTC+5:30); precipitation sums included.

## Measured variables and data structure
- Meteorological: Pa, Ta, RH, SWin, SWout, LWin, LWout, Rnet, Precipitation, WS, WD.
- Soil physics: G1, G2 (0.03 m depth), Tsoil_0.05_1, Tsoil_0.15_1, Tsoil_0.05_2, Tsoil_0.15_2; VWC_0.05_1, VWC2_0.15_1, VWC1_0.05_2, VWC2_0.15_2.
- Data files: one CSV per station; complete time series; missing data marked as -9999; end-of-period timestamps reflect 1-minute interval.
- Site metadata: instrument models, sensor heights, and sampling locations; Table 2 describes variables and units.

## Data quality and handling
- QC processes: basic range checks, spike/dropout visual checks, cross-checks between soil depth measurements, and rainfall corroboration for abrupt soil moisture changes.
- Clearly erroneous data removed; large changes in soil moisture cross-checked with rainfall and flood events (Kanpur).
- Data gaps acknowledged with -9999 markers.

## Data format and governance considerations
- Data format: CSV files with standardized, time-stamped records; timestamps end of each one-minute period; time zone is Indian Standard Time.
- Metadata and provenance: detailed site descriptions, sensor configurations, and sampling regimes documented to support data reuse and governance.
- Acknowledgments: funding and collaborations acknowledged; site owners acknowledged for access and permissions.
- Reuse considerations: comprehensive description of measurement units, depths, and locations facilitates data discovery, interoperability, and discovery by data users.

## Practical implications for data stewards
- Rich, high-temporal-resolution dataset with clear QC and complete site metadata supports reproducibility and cross-site analyses.
- Clear handling of missing data and documentation of instrumentation supports governance, data discovery, and ongoing updates or reprocessing if needed.
- Potential for integration with other INCOMPASS datasets to enhance atmospheric-surface interaction studies across diverse Indian terrains.