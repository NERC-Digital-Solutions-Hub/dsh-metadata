# Supporting documentation for: Daily and sub-daily hydrometeorological and soil data (2013-2023) [COSMOS-UK]

- A comprehensive COSMOS-UK dataset spanning 51 sites (2013–2023) with sub-hourly and daily hydrometeorological and soil data, metadata, and quality information.
- Data produced and described by Smith et al. (2024), hosted in the NERC Environmental Information Data Centre; COSMOS-UK is part of UK-SCAPE National Capability.

## Overview of data products and structure

- Total files: 258 items, organized as:
  - 1 COSMOS-UK site metadata file (COSMOS-UK_SiteMetadata_2013-2023.csv)
  - 51 Sub-hourly hydrometeorological and soil data files (COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>-2023.csv)
  - 51 Sub-hourly QC flags files (COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>-2023_QC_Flags.csv)
  - 51 Sub-hourly data flags files (COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>--2023_Flags.csv)
  - 1 Sub-hourly data metadata file (COSMOS-UK_HydroSoil_SH_2013-2023_Metadata.csv)
  - 51 Daily hydrometeorological and soil data files (COSMOS-UK_<SITE ID>_HydroSoil_Daily_<YEAR SITE OPENED>-2023.csv)
  - 51 Daily data flags files (COSMOS-UK_<SITE ID>_HydroSoil_Daily_<YEAR SITE OPENED>--2023_Flags.csv)
  - 1 Daily data metadata file (COSMOS-UK_HydroSoil_Daily_2013-2023_Metadata.csv)

- Data scope and cadence:
  - Sub-hourly (SH) data at 30-minute resolution from Oct 2013 to Dec 2023.
  - Daily (D) derived data (including VWC, potential evapotranspiration, SWE) from Oct 2013 to Dec 2023.
  - A wide range of variables captured, with many derived from sub-hourly measurements.

- Data availability and formats:
  - Missing values represented as -9999 (sub-hourly and daily).
  - SH data timestamps end of 30-minute periods (e.g., 12:30 refers to 12:00–12:30 interval).
  - Derived and QC/flag files mirror the structure of their data files with suffixes _QCFLAG and _FLAG.

## Spatial and site metadata

- 51 COSMOS-UK sites with coordinates and site attributes (easting, northing, various projections, altitude, soil type, land cover, bulk density, soil carbon, lattice water).
- Site metadata includes:
  - SITE_ID (unique 5-character code), SITE_NAME
  - START_DATE and END_DATE (END_DATE present for decommissioned sites)
  - Spatial coordinates and projections (OSGB36 and WGS84 references)
  - Soil and land cover characteristics and soil properties (bulk density, soil organic carbon, lattice water)
- Decommissioned sites noted: Wytham Woods (2016-10-01), Redmere (2018-09-20), Cochno (2020-11-16), Harwood Forest (2022-06-28).
- Altitude data mainly sourced from NEXTMap 10 m DTM; some sites have altitude estimates due to data gaps or accuracy considerations.

## Sub-hourly data (SH)

- Variables and structure:
  - A comprehensive set of meteorological and soil variables (radiation components, precipitation, air temperature, humidity, pressure, wind, soil temperature, soil moisture at multiple depths, heat fluxes, etc.).
  - SH_Variables are documented in the SH metadata file; SH data include 30-minute aggregations (mean or sum as specified).
- Data quality and QC:
  - Two-stage QC: automated QC tests (flagging and removal) and daily visual inspection.
  - QC flags (per data point) indicate which QC tests were failed; combined values are additive to yield a unique final QC flag.
  - QC flags file mirrors the SH data file with _QCFLAG suffix.
  - Data flags file (COSMOS-UK_<SITE>_HydroSoil_SH_..._Flags.csv) describes data point status (Missing, Unchecked, Infilled, Estimated) with _FLAG suffix.
  - Net radiation RN and absolute humidity Q are derived from QC’d data and are not themselves QC-tested.
- Data usage notes:
  - QC flags help interpret why data were removed; data flags indicate infilled or estimated values.
  - Presence of inflow of QC flags alongside data values allows traceability of data quality issues.

## Daily data

- Derived daily products (Oct 2013–Dec 2023):
  - Volumetric water content (VWC) from CRNS (COSMOS_VWC), snow water equivalent (SWE), and potential evapotranspiration (PE).
  - Radiation balance components and associated daily aggregates.
- Data content and units:
  - LWIN, LWOUT, SWIN, SWOUT: solar radiation components in MJ/m^2/day.
  - RN, PRECIP, PRECIP_TIPPING, PRECIP_RAINE, PA, TA, WS, WD, Q, RH, G1, G2, TDT*_TSOIL, TDT*_VWC, STP_TSOIL*, etc., with daily aggregations (some means, some totals) as specified.
  - G1/G2: soil heat flux components; TDT sensors provide soil temperature and VWC at multiple depths; STP_TSOIL depths cover 2, 5, 10, 20, 50 cm.
  - COSMOS_VWC: daily VWC derived from CRNS data with calibration and correction steps described in the method sections.
  - SWE: daily snow water equivalent derived from CRNS counts, albedo-based snow day identification, and a dedicated method.
  - PE: daily potential evapotranspiration calculated via Penman-Monteith (requires RN, G1/G2, TA, RH, WS, PA).
  - GCC: daily green colour content derived from PhenoCam images; processed using site-specific masks; note: GCC data have not undergone quality control.
- Completeness and QC:
  - Daily data are derived from QC’d sub-hourly data; no separate daily QC is applied.
  - Daily data flag files accompany the daily data, mirroring their structure.

## Infilling

- Infilling approach:
  - Interpolation used for gaps considered reasonable, applied to selected variables.
  - Two interpolation methods: linear and order-2 polynomial (depending on gap size and surrounding data).
  - Gap assessment guided by: gap length (≤ 10 values), number of surrounding points, and method performance (RMSE).
  - RMSE-based selection: an internal process uses artificial gaps to evaluate method performance and selects the best approach per variable.
- Impact on data:
  - Infilling values are flagged (I in the data flags) to indicate interpolation-based estimates.

## Completeness

- Overall completeness metrics per site:
  - Met: aggregation of key meteorological variables (precipitation, humidity, air temperature, pressure, radiation, wind, etc.).
  - Soil: aggregation of soil measurements (soil heat flux, soil temperature, and VWC from TDT sensors).
  - VWC completeness: derived VWC completeness from CRNS-based VWC data.
- Completeness assessed for the period Oct 2013–Dec 2023.

## Instrumentation and site setups

- Core instrument types:
  - Cosmic-Ray Neutron Sensor (CRNS) for VWC and related derived products.
  - Rain gauges: OTT Pluvio 2 (for accumulation, with caveats on wind-induced undercatch and height adjustments) and tipping-bucket rain[e] devices.
  - Point soil moisture sensors (TDT-based) at multiple depths; soil temperature sensors at several depths.
  - Radiometer (upward/downward shortwave and longwave components); net radiation derived from components.
  - Wind sensors: 3D sonic anemometers or integrated WindSonic for wind speed and direction.
  - PhenoCam for GCC (green colour content) derived from daily max image; note: GCC data lack QC.
- Site variation:
  - 7. Instrumentation sections detail which sites have snow sensors, full TDT arrays, anemometers, tipping buckets, rain[e], and AWS configurations (GILL MetPak vs Vaisala).
  - Rain[e] height adjustments occurred in 2023 to reduce blockage risk, raising rim height to 1.0 m at many sites; adjustments and dates are documented.

## SNOW and related derived data (4.5.X)

- SWE and snow days:
  - Snow days identified via albedo thresholds (10:00–14:00 GMT average albedo > 50% for start, < 35% for end).
  - SWE estimated from daily CRNS counts compared to snow-free conditions (Method 1 in Wallbank et al. 2020).
- Albedo, GCC, and CRNS-derived products:
  - GCC derived from PhenoCam imagery using site masks; daily GCC is the maximum value across a day.
  - Albedo and SWE are derived as described; GCC has no quality control.

## Changes to data (major revisions)

- Data processing and recalibration activities:
  - 2024: Daily PE data fix; site altitude metadata updates; VWC calibration updates; bulk density recalibration; various associated variable recalculations.
  - 2023–2022: Reprocessing events including VWC calibration updates, pressure sensor recalibration corrections, and rain[e] height-related data corrections.
  - 2020–2019: Various improvements to PE calculation, CRNS-related processing (including infilling from secondary tubes), NMDB data infill, and precipitation data updates.
  - 2019–2020: SWE addition and daily albedo calculations introduced.
- Each change includes date(s) and the affected data variables.

## Author contributions and references

- Principal author and data manager: R. Smith; collaborative team responsible for data processing, site metadata, instrumentation, and data processing algorithms.
- References include foundational works on CRNS calibration, soil moisture and energy balance methods, and related radiometric and meteorological methodologies (Baatz et al., Bogena et al., Desilets et al., Köhli et al., Wallbank et al., Zreda et al., FAO, etc.).