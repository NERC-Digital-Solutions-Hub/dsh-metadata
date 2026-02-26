# COSMOS-UK Daily and sub-daily hydrometeorological and soil data (2013-2019) [COSMOSUK]. NERC Environmental Information Data Centre.

## Overview
- A multi-resolution dataset (sub-hourly, hourly, daily) of hydrometeorological and soil moisture data from 51 COSMOS-UK sites, 2013–2019.
- Total of 208 files including site metadata, per-site data files, and QC metadata/flags.
- Data are intended for analysis and mapping of hydrology and soil moisture across the COSMOS-UK network; suitable for GIS-enabled visualization and spatial analyses when joined with site metadata.

## Spatial coverage and data products
- 51 COSMOS-UK sites across the UK with spatial coordinates and site attributes in a dedicated metadata file.
- Site coordinates provided in OSGB36 (EASTING/NORTHING) and WGS84 (LAT/LONG) with altitude.
- Data products include:
  - Sub-hourly (30-minute) hydro-soil data with QC flags
  - Hourly hydro-soil data (including VWC from CRNS and TDT sensors)
  - Daily hydro-soil data (including VWC, potential evapotranspiration, and snow water equivalent)
  - Associated metadata and QC flag files per site

## Data files and organization
- 208 files in total, organized by data type and per site.
- Key file groups:
  - COSMOS-UK_SiteMetadata_2013-2019.csv – site locations, coordinates, soil type, land cover, and site-level attributes
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2019.csv – sub-hourly (30-min) data
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2019_Metadata.csv – sub-hourly metadata
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2019_QC_Flags.csv – sub-hourly QC flags
  - COSMOS-UK_<SITE_ID>_HydroSoil_Hourly_2013-2019.csv – hourly data
  - COSMOS-UK_<SITE_ID>_HydroSoil_Hourly_2013-2019_Metadata.csv – hourly metadata
  - COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2019.csv – daily data
  - COSMOS-UK_HydroSoil_Daily_2013-2019_Metadata.csv – daily metadata
- Data values use -9999 as missing; timestamps for sub-hourly are end-of-interval (e.g., 12:30 covers 12:00–12:30).

## Data content by resolution

- Sub-hourly (30-minute) data
  - Variables: hydrometeorological (radiation, precipitation, pressure, temperature, humidity, wind components and direction, absolute humidity, relative humidity), soil measurements (soil temperature and volumetric water content at multiple TDT depths), snow depth, snow-related counts, soil heat flux (G1, G2), and wind components (UX, UY, UZ)
  - Also includes snow depth sensor counts and error/diagnostic fields
  - Wind components and some sensors vary by site (e.g., not all depths or directions present at all sites)
  - Data come with a two-stage QC process and per-variable QC flags

- Hourly data
  - Volumetric water content (VWC) derived from CRNS with corrected neutron counts
  - Includes COSMOS_VWC (soil moisture), D86_75m (effective depth from CRNS), and hourly VWC at the CRNS-derived depths
  - Additional hourly variables derived from sub-hourly measurements and processing (e.g., CRNS-derived VWC with corrections)

- Daily data
  - VWC daily mean (COSMOS_VWC), D86_75m daily mean, potential evapotranspiration (PE), snow water equivalent (SWE) and snow days indicator, albedo
  - SWE estimation uses snow-detection via albedo (between 10:00–14:00) and counts-based snow-free correction
  - PE calculated via Penman-Monteith using sub-hourly inputs (RN, G, TA, RH, WS, PA)
  - Date stamp indicates 00:00 start of the day (covering the preceding 24 hours)

## Methodologies and data provenance
- VWC derived from Cosmic-Ray Neutron Sensor (CRNS) counts, corrected for atmospheric pressure, humidity, and cosmic-ray intensity (NMDB reference) and using site-specific N0 calibrations.
- Corrections account for lattice water, bound water, and soil organic carbon as appropriate per site.
- An extra 2018 correction factor applied to counts to address spurious trends in VWC data.
- SWE estimation and albedo-based snow days are described in the methodology (Wallbank et al. 2020; Evans et al. 2016; Köhli et al. 2015).
- PE derived from Penman-Monteith using sub-hourly data.

## Quality control and completeness
- Two-stage QC process:
  - Automatic QC tests applied on the server-side processing script; failing data are flagged and removed
  - Daily visual inspection of data via automated plots
- QC flags are stored in separate per-site QC files; flags are additive to create a unique final value describing all tests failed
- QC flag descriptions cover missing data, zero values, insufficient samples, low power, sensor faults, diagnostic flags, out-of-range values, secondary variable concerns, spikes, and other errors
- QC flags maintained with corresponding -QCFLAG columns in QC files
- Completeness varies by site and variable; a dedicated completeness section (Table 6.1) provides site-level completeness across Met, Soil, and VWC groups

## Instrumentation (overview)
- Cosmic-Ray Neutron Sensor (CRNS) – soil moisture via neutron counts; field calibration and corrections described
- Rain gauge (OTT Pluvio) – precipitation measurement with site-specific corrections
- Point soil moisture sensors (TDT) – measure soil moisture and soil temperature at various depths
- Soil heat flux plates (G1, G2) – measure soil heat flux
- Soil temperature sensors (TDT/STP) – multi-depth temperature profiling
- Radiometer (NR01) – net, shortwave, and longwave radiation components
- Automatic weather station – air temperature, relative humidity, and barometric pressure
- Barometric pressure sensor – supports corrections for CRNS and other calculations
- Humidity and temperature sensors (Vaisala HUMICAP) – supplement measurements
- 3D and integrated sonic anemometers – wind speed and direction
- Snow depth sensor (SR50A) and SnowFox – snow-related measurements and SWE estimation
- Data logger (CR3000) – central data acquisition and telemetry

## Changes to data and versioning
- Ongoing data processing improvements; when changes occur, full time series are reprocessed
- Notable changes include:
  - 2021: D86_75m correction
  - 2020: VWC calibration updates; CRNS counts infill from secondary tubes and NMDB data infill; refinement of 30-min precipitation and PE computations
  - 2019: SWE added; daily albedo added
  - Ongoing updates to 30-min data processing and aggregation methodology

## Access, usage, and integration notes
- Datasets are designed for GIS and map-based visualization; join per-site data with COSMOS-UK site metadata for spatial analyses
- Metadata files provide the mapping between SITE_ID and site coordinates, enabling spatial aggregation and visualization
- Time stamps align with end-of-interval conventions for sub-hourly data; daily data use 00:00 of the day as the period start
- Data quality is documented via QC flags; flagged values are removed from primary data but logged in QC files for traceability
- Full COSMOS-UK User Guide and updates are available from the COSMOS-UK website

## Author contributions and references
- Stanley et al. (2021) compilation and documentation; data managers and instrument teams responsible for data quality, calibration, and site maintenance
- Key references include foundational methods for CRNS-derived VWC, calibration approaches, and SWE estimation (e.g., Baatz et al. 2014; Zreda et al. 2012; Evans et al. 2016; Wallbank et al. 2020)

## References (selected)
- Baatz et al. 2014; Bogena et al. 2015; Desilets et al. 2010; Franz et al. 2012, 2013; Zreda et al. 2012
- Evans et al. 2016; Köhli et al. 2015; Wallbank et al. 2020
- FAO Penman-Monteith (FAO 56, 1998)
- COSMOS-UK project documentation and user guide (Stanley et al. 2021)