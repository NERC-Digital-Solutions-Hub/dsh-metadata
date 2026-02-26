# Daily and sub-daily hydrometeorological and soil data (2013-2023) [COSMOS-UK]

## Overview
- COSMOS-UK provides 51 sites of daily and sub-hourly hydrometeorological and soil moisture data from 2013 to 2023.
- Total dataset comprises 258 files: site metadata, 51 sub-hourly data files, 51 sub-hourly QC flags, 51 sub-hourly data flags, 1 sub-hourly metadata, 51 daily data files, 51 daily data flags, and 1 daily metadata.
- Sub-hourly data are at 30-minute resolution; daily data include derived metrics such as volumetric water content (VWC), snow water equivalent (SWE), potential evapotranspiration (PE), and albedo-derived GCC.
- VWC is derived from Cosmic-Ray Neutron Sensor (CRNS) measurements; SWE and daily PE are derived from sub-hourly data and CRNS. PhenoCam provides GCC data.

## Data structure and contents
- 1 site metadata file: COSMOS-UK_SiteMetadata_2013-2023.csv with site-specific details (location, soil, land cover, bulk density, carbon, etc.). Note: several sites decommissioned (e.g., Wytham Woods, Redmere, Cochno, Harwood Forest).
- Sub-hourly data: COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>-2023.csv (30-min data per site) and corresponding QC (…_QC_Flags.csv) and data flags (…_Flags.csv); 30-min end timestamps applied (e.g., 12:30 refers to 12:00:01–12:30:00).
- Sub-hourly metadata: COSMOS-UK_HydroSoil_SH_2013-2023_Metadata.csv describing variables and units.
- Daily data: COSMOS-UK_<SITE ID>_HydroSoil_Daily_<YEAR SITE OPENED>-2023.csv (derived metrics like VWC, SWE, PE, SWE-derived daily albedo, GCC);  daily flags and metadata files analogous to sub-hourly.
- Daily metadata: COSMOS-UK_HydroSoil_Daily_2013-2023_Metadata.csv.
- All missing values coded as -9999 in data files.

## Data coverage and scope
- 51 COSMOS-UK sites (locations mapped in site metadata); 2013–Dec 2023 records.
- Sub-hourly data include a comprehensive set of meteorological and soil measurements (radiation, precipitation, air temperature, humidity, pressure, wind, soil temperature and moisture at multiple depths, heat fluxes, etc.).
- Daily data include derived VWC, SWE, PE, albedo, and GCC; VWC uses CRNS-derived methods with corrections for pressure, humidity, and cosmic-ray intensity.
- Some site data and equipment configurations vary over time; full instrumentation details are provided.

## Sub-hourly data specifics
- Variables include LWIN, LWOUT, SWIN, SWOUT, RN (net radiation), PRECIP types (Pluvio, tipping bucket, rain[e], etc.), PA (pressure), TA (air temp), WS/WD (wind speed/direction), Q and RH, SNOW_DEPTH, soil sensors (TDT and VWC at multiple depths), G1/G2 soil heat flux, STP_TSOILx and STP_VWC for various depths, and COSMOS_VWC and related CRNS-derived parameters.
- RN and Q are not subjected to QC tests.
- Data are quality controlled via:
  - Automatic QC tests with specific flags (0 = pass; non-zero flags indicate failures); tests include missing data, zero values, too few samples, low power, sensor fault, diagnostic, out of range, secondary variable, midnight calibration, spike, and error codes.
  - Daily visual QC plots.
- QC flags are stored in separate files mirroring data structure; data flags (M = missing but not infilled, U = unchecked, I = infilled, E = estimated) accompany data values to indicate data quality and infilling status.

## Daily data specifics
- Derived data include VWC (CRNS-based), SWE (from CRNS with albedo-based snow detection), PE (Penman-Monteith using RN, G1/G2, TA, RH, WS, PA), and GCC (from PhenoCam imagery with site masks; not quality-controlled).
- VWC/SWE are generated at daily resolution; SWE is a midday value; GCC is the daily maximum of green color content.
- Daily data are derived from sub-hourly data and thus inherit sub-hourly QC; daily data do not have separate QC beyond derivation from QC’d sub-hourly data.
- A separate daily data flags file exists to document infilling/estimation at the daily level.

## Infilling
- Infilling uses interpolation for gaps deemed reasonable (e.g., small gaps or variables with low variability).
- Two interpolation methods: linear and order-2 polynomial; method selection depends on gap size and surrounding data.
- RMSE-based evaluation uses 5000 artificial gaps to select the best method for each variable.
- Infilling is applied to selected sub-hourly and daily variables; details provided in dedicated sections.

## Completeness
- Completeness metrics cover Met (precipitation, humidity, air temperature, pressure, radiation, wind) and Soil (soil heat flux, soil temperature, VWC from TDT sensors); VWC completeness reflects CRNS-derived data.
- Figures summarize site-level completeness across the dataset period.

## Instrumentation
- COSMOS-UK uses a suite of instruments, with variations by site and over time:
  - Cosmic-Ray Neutron Sensor (CRNS) models: Hydroinnova CRS-2000/B and CRS-1000/B.
  - Rain gauges: OTT Pluvio 2; tipping bucket rain gauge (SBS500); rain[e] weighing rain gauge.
  - Soil moisture sensors: Time Domain Transmissometry (TDT) probes (depths including 10 cm, 5 cm, 15 cm, 25 cm, 50 cm depending on depth arrays).
  - Soil heat flux: Hukseflux HFP01SC.
  - Soil temperature sensors: Hukseflux STP01 (multiple depths).
  - Radiometer: Hukseflux NR01 (shortwave/longwave components; net radiation derived).
  - Airborne sensors: Rotronic HC2A-S3, Gill MetPak or Vaisala sensor suites (temperature, humidity, pressure).
  - 3D sonic anemometer or integrated WindSonic for wind speed/direction.
  - PhenoCam: Mobotix S14 for GCC (greenness) estimates.
  - Snow sensors: SR50A snow depth; SnowFox sensor for SWE derivation.
  - Data logger and processing: Campbell Scientific CR3000.
- 7.2 site variations document differences in installations and instrument upgrades; 7.2.1 notes adjustments to rain[e] height (raising to 1.0 m to reduce blockages) at several sites.

## Data changes and curation
- The dataset undergoes ongoing reprocessing to improve data quality:
  - 2024: Daily PE data fix; site altitude metadata updated.
  - 2023–2024: VWC calibration updates, bulk density recalibration, and related recalculations (N0_MOD, N_MIN, N_MAX).
  - 2023: 00:30 and 01:00 heat flux data (G1/G2) removal due to midnight calibration spikes; infilling applied to gaps < 10 data points (air temp, RH, PA, soil heat fluxes, radiation, wind, etc.).
  - 2020–2021: CRNS-related data infilling; VWC recalibration; NMDB data infilling.
  - 2019–2020: SWE added; daily albedo added; PE methodology updates.
- Data reprocessing implies that time series may be revised; users should reference the latest version and changelog when analyzing trends.

## Access and references
- COSMOS-UK website for network information and user guides: https://cosmos.ceh.ac.uk/
- Data are published under NERC Environmental Information Data Centre; dataset is part of the COSMOS-UK project (NE/R016429/1; UK-SCAPE National Capability).
- Primary author and data stewardship: R. Smith; multiple contributors manage site metadata, data processing, and technical maintenance.
- Primary reference: Smith et al. (2024) with detailed methodology and data processing references.

## Key takeaways for data leadership
- A wide, well-documented, quality-controlled, multi-site dataset of 30-minute sub-hourly and daily hydrometeorological and soil data across 51 COSMOS-UK sites (2013–2023), with comprehensive metadata, QC, and data-flagging mechanisms to support governance and governance-friendly reuse.
- Derived data (VWC from CRNS, SWE, PE, GCC) enable integrated analyses of soil moisture, energy balance, and vegetation phenology, subject to cryogenic and calibration updates; data are reprocessed as methods improve.
- Robust data quality framework: two-stage QC, detailed QC flags, and separate data flags to distinguish infilled/estimated data, enabling transparent data provenance.
- Instrumentation and site configurations are documented, with site-specific variations and 2023–2024 adjustments (e.g., rain[e] height) noted to ensure data comparability.
- Data completeness and calibration updates are tracked; users should consider reprocessed data updates and consult changelog when performing longitudinal analyses.