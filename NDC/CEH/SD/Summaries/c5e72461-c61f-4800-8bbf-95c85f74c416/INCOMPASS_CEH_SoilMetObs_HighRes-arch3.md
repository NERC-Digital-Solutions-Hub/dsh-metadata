# High temporal resolution meteorology and soil physics observations from INCOMPASS land surface stations in India, 2016 to 2018

- Overview
  - A dataset of one-minute time-series observations of meteorological and soil-physics variables from three INCOMPASS Land Surface Stations in India.
  - Time period: 2016-01-01 00:01 to 2019-01-01 00:00 (end: 2018-08-28 06:23 for Kanpur).
  - Sites: Berambadi (southern Karnataka, agricultural land), Dharwad (northern Karnataka, agricultural campus), Kanpur (semi-natural grassland, IIT Kanpur, Uttar Pradesh).
  - Purpose within the INCOMPASS project: to study convective organization, monsoon precipitation, atmosphere, surface and sea interactions.

- Study sites and locations
  - Berambadi: 11.760633°N, 76.585361°E, 873 m amsl; semi-arid tropical monsoon climate (Aw); Alfisol soils; mixed agriculture.
  - Dharwad: 15.498393°N, 74.985730°E, 692 m amsl; tropical savannah climate (Aw); Vertisol soils; agriculture-dominated surroundings.
  - Kanpur: 26.509072°N, 80.223765°E, 129 m amsl; humid subtropical climate (Csa); Fluvisol soils; semi-natural grassland with seasonal flooding.

- Sampling regime and instrumentation
  - Automated measurements at 1-minute resolution using identical instrumentation across all stations.
  - Meteorological measurements from a 10 m mast; sensors include barometric pressure, air temperature, relative humidity, net radiation and components, wind speed/direction, and precipitation (tipping bucket, 1.0 m height).
  - Soil physics measurements duplicated at two locations/depths: soil heat flux at 0.03 m; soil moisture and temperature at 0.05 m and 0.15 m depths.
  - Data logged at 0.1 Hz and aggregated to one-minute means; precipitation sums are per minute.

- Data quality control and structure
  - QC includes basic range checks, spike/dropout visual checks, cross-checks between depths and with rainfall/flooding (notably at Kanpur).
  - Clearly erroneous data removed; missing data coded as -9999.
  - Data provided as a CSV file per station; timestamps are end-of-minute; metadata and variable descriptions defined in accompanying tables.

- Variables and units (selected)
  - Met variables: Pa (kPa), Ta (°C), RH (%), SWin, SWout, LWin, LWout, Rnet (W m^-2), Precipitation (mm min^-1), WS (m s^-1), WD (degrees).
  - Soil heat flux: G1, G2 (W m^-2) at 0.03 m depth.
  - Soil temperature: Tsoil_0.05_1, Tsoil_0.15_1, Tsoil_0.05_2, Tsoil_0.15_2 (°C).
  - Soil moisture: VWC_0.05_1, VWC2_0.15_1, VWC1_0.05_2, VWC2_0.15_2 (%).
  - Data quality flags: -9999 for missing records.

- Temporal coverage and data availability
  - Berambadi and Dharwad: 2016-01-01 to 2019-01-01.
  - Kanpur: 2016-01-01 to 2018-08-28 06:23 (end-of-file due to project timing).

- Data structure and access considerations for monitoring frameworks
  - Standardized, high-temporal-resolution data across multiple representative land-use types (agricultural, campus agriculture, and semi-natural grassland) enabling cross-site comparisons.
  - Comprehensive metadata on locations, soils, climate context, and instrument specifics to support data provenance and reproducibility.
  - Clear documentation of units, sensor depths, and measurement cadence aids in data harmonization and integration into monitoring dashboards, indicators, and decision-support tools.
  - Potential limitations to consider in frameworks: data gaps (notably Kanpur end date), site-specific environmental conditions (flooding, fires), and reliance on -9999 coding for missing data that requires handling in analyses.

- Acknowledgments and references
  - Funded by UK MoES and related UK-India collaborations; acknowledges site owners and collaborators.
  - References to climate classifications and regional data sources used for site descriptions.