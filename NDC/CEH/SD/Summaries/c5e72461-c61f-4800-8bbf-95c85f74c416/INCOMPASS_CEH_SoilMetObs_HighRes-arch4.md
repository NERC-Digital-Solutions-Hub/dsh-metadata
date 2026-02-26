# High temporal resolution meteorology and soil physics observations from INCOMPASS land surface stations in India, 2016 to 2018

## Overview
- A dataset of one-minute time series observations of meteorology and soil physics variables from three INCOMPASS Land Surface Stations in India.
- Data collection period: 2016-01-01 00:01 to 2019-01-01 00:00 (Kanpur ends 2018-08-28 06:23).
- Locations: Berambadi (southern Karnataka), Dharwad (northern Karnataka), and Kanpur (Uttar Pradesh).
- Purpose: support understanding of land-atmosphere interactions under different Indian climates and land uses.

## Sites and characteristics
- Berambadi, Southern Karnataka
  - Location: agricultural land on the Deccan Plateau, near Western Ghats foothills.
  - Climate: semi-arid tropical monsoon (Aw); mean annual temp ~24.4°C; ~600 mm rainfall.
  - Soils: Alfisols; dominant crops include maize, turmeric, sunflowers, marigold, sorghum, vegetables.
  - Elevation: ~873 m; coordinates ~11.7606°N, 76.5854°E.
- Dharwad, Northern Karnataka
  - Location: agricultural campus of the University of Agricultural Sciences, Dharwad.
  - Climate: tropical savannah (Aw); mean annual temp ~24.3°C; ~885 mm rainfall.
  - Soils: Vertisols; flat field with long-term agricultural management.
  - Elevation: ~692 m; coordinates ~15.4984°N, 74.9857°E.
  - Surrounding crop schedule includes maize, intercropping (soybean, pigeon pea), and rotations.
- Kanpur, Uttar Pradesh
  - Location: semi-natural grassland within IIT Kanpur campus.
  - Climate: humid subtropical (Csa); mean annual temp ~25.6°C; ~820 mm rainfall; monsoon Jun–Oct.
  - Soils: Fluvisols (silty alluvium); Indo-Gangetic Plain; grassland subject to seasonal flooding.
  - Elevation: ~129 m; coordinates ~26.5091°N, 80.2238°E.
  - Vegetation: Phragmites-Saccharum-Imperata grassland; surface water intermittently present.

## Sampling regime and instrumentation
- Measurements were taken with identical instrumentation at all three sites.
- Meteorology: measured from 10 m masts; sensors include barometric pressure, air temperature, relative humidity, net radiation and components, wind speed and direction, precipitation.
- Soil physics: duplicated measurements at two locations per site, at two depths (0.05 m and 0.15 m) for soil moisture and temperature; soil heat flux measured at 0.03 m depth at two locations.
- Data logging: sensors scanned at 0.1 Hz and logged as one-minute means; precipitation logged as sums per minute.
- Data quality control: basic range checks, spike/dropout detection; cross-checks of soil measurements against paired soil observations and rainfall/flooding events; clearly erroneous data removed.

## Data structure and variables
- Data format: one CSV file per site.
- Time indexing: timestamps are end-of-interval and recorded in Indian Standard Time (IST, UTC+5:30).
- Key variables (per Table 2 description):
  - Pressure (Pa, but stored as kPa in table) and weather variables: Ta (air temperature, °C), RH (%), SWin, SWout, LWin, LWout, Rnet (W/m²), Precipitation (mm/min), WS (m/s, wind speed at 10 m), WD (degrees, wind direction from north).
  - Soil heat flux: G1, G2 (W/m²) at 0.03 m depth, location 1 and 2.
  - Soil temperature: Tsoil_0.05_1, Tsoil_0.15_1, Tsoil_0.05_2, Tsoil_0.15_2 (°C).
  - Volumetric water content: VWC_0.05_1, VWC2_0.15_1, VWC1_0.05_2, VWC2_0.15_2 (% at respective depths/locations).
- Missing data: indicated by -9999.
- Sensor specifics: common instrumentation across sites (LI-7500A, HMP155 shield, NR01 net radiometer, WindSonic, SBS314 rain gauge, and soil sensors from HFP01-SC and ACC-SEN-SDI).

## Data quality, governance, and notes for data management
- Quality control implemented for meteorological data and cross-validated soil measurements against depths and rainfall, with outliers removed.
- Data are accompanied by site-level metadata on location, climate context, soil types, land use, and surrounding management practices, aiding discoverability and appropriate use.
- Temporal coverage includes three diverse sites with different land uses and climates, enabling cross-site comparisons and regional synthesis.
- Data limitations:
  - Kanpur site ends earlier (2018-08-28 06:23) than other sites, creating a gap in full three-site simultaneous coverage for part of the period.
  - Some records may be missing due to system issues, indicated by -9999.
- Documentation and provenance:
  - Data generated under the INCOMPASS project; acknowledgments include funding sources and contributor institutions.
  - Data hosted with explicit variable definitions, units, and time standardization to facilitate reuse and integration with other datasets.

## Relevance for data leadership and use
- Demonstrates a well-documented, high-resolution, multi-site meteorology and soil physics dataset with clear QC procedures, metadata, and data structure—exemplary for establishing data governance models.
- Useful for exploring data discovery, metadata completeness, and cross-site data integration in complex, real-world observational networks.
- Supports analyses of energy balance, soil moisture dynamics, and land-atmosphere coupling across contrasting Indian ecosystems, with potential for informing policy-relevant climate and agricultural studies.
- Highlights practical considerations for data access, update cadence, and handling of missing data in large observational datasets.