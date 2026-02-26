# Daily and sub-daily hydrometeorological and soil data (2013-2022) [COSMOSUK]

## Overview
- Comprehensive dataset from the COSMOS-UK network covering 51 sites, 2013–2022.
- Contains 258 files comprising site metadata, sub-hourly and daily hydrometeorological and soil data, and quality/completeness information.
- Data are intended for discovery and reuse, with provenance and quality controls documented to support data governance and reliable use by researchers and practitioners.
- Primary repository: NERC Environmental Information Data Centre; network information and user guidance available via the COSMOS-UK site.

## Data structure and contents
- Sub-hourly data (30-minute resolution) and associated metadata and flags:
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022.csv (data)
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_Metadata.csv (variable definitions)
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_QC_Flags.csv (QC flag details)
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_Flags.csv (data flags)
- Daily data and flags:
  - COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2022.csv (derived daily metrics)
  - COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2022_Metadata.csv
  - COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2022_Flags.csv
- Site-level metadata:
  - COSMOS-UK_SiteMetadata_2013-2022.csv, including site name, coordinates, start/end dates, soil type, land cover, bulk density, soil organic carbon, lattice water, etc.
  - Decommissioned sites noted (e.g., Wytham Woods, Redmere, Cochno, Harwood Forest) with end dates.
- Data characteristics:
  - Missing values are encoded as -9999 (sub-hourly and daily data).
  - Timestamps are end-of-interval (e.g., 12:30 for 12:00–12:30).
  - Data telemetered hourly to UKCEH central system.

## Variables and data foundations
- Sub-hourly (30-min) data include: radiation (LWIN, LWOUT, SWIN, SWOUT, RN), precipitation (PRECIP, PRECIP_TIPPING, PRECIP_RAINE), atmospheric (PA, TA, RH, Q), wind (WS, WD, UX/UY/UZ), soil and heat flux (G1, G2, TDT soil temps and VWC at various depths, STP_TSOIL, STP_VWC, COSMOS_VWC, SWE, PE, GCC, albedo, etc.).
- Daily data derive: volumetric water content (VWC) from CRNS (COSMOS_VWC) with corrections for background cosmic ray intensity, altitude, atmospheric pressure, and absolute humidity; snow water equivalent (SWE) and albedo; potential evapotranspiration (PE) via Penman-Monteith; various daily radiation and meteorological composites; GCC (green colour content) from PhenoCam imagery.
- Special notes:
  - VWC derived from CRNS requires corrections and calibrations (CTS_MOD_CORR, N0_MOD, etc.); albedo and SWE are linked to snow detection logic using daily albedo thresholds.
  - GCC is derived from PhenoCam imagery using site masks; daily GCC is the maximum value of the day; GCC data are not quality-controlled.

## Quality control and data quality management
- Two-stage QC process:
  - Automated QC tests applied via processing script; failing data are flagged and removed. Each test has a unique flag value; multiple flags can be combined.
  - Daily visual inspection of data via automated plots.
- QC flags (for sub-hourly data) indicate reasons for removal (e.g., missing, out of range, low power, sensor fault, spike, diagnostic, etc.). Net radiation (RN) and absolute humidity (Q) are not subjected to QC tests because they are derived from QC’d inputs.
- QC flag files mirror data files with _QCFLAG suffix; QC flags reveal the reason for data removal when non-zero.
- Data flags (COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_Flags.csv) describe the data quality status of each value (Missing, Unchecked, Infilled, Estimated). Data flags help interpret the presence and reliability of values, including infilling and estimation status.
- Data provenance:
  - QC flags explain why data were removed; non-zero QC flags indicate infilled or estimated data in the corresponding data value.
  - Data flags provide information about infilling or estimation status, offering a practical view of data usability.

## Infilling (gap-filling)
- Infilling is applied to selected variables for gaps deemed reasonable.
- Methods: linear interpolation and order-2 polynomial interpolation.
- Decision logic for method choice based on gap size and surrounding data:
  - Gap size ≤ 10 points may allow linear or polynomial; larger gaps may use more surrounding points.
  - RMSE-based selection: 5000 artificial gaps are used to evaluate method performance and select the best method for each variable.
- Infilling details are applied only to variables chosen for infilling (as listed in the metadata and tables).

## Completeness and coverage
- The dataset provides completeness statistics across sites for the study period (October 2013 to December 2022).
- Met (precipitation, humidity, air temperature, atmospheric pressure, short/longwave radiation, wind) and Soil (soil heat flux, soil temperature, and TDT-based soil moisture) groups summarize overall data completeness.
- Derived VWC data (cosmos VWC) completeness is reported separately.
- Completeness varies by site; full site-level completeness tables are provided in the documentation.

## Instrumentation and site configurations
- Core instrumentation (section 7.1) includes:
  - Cosmic-Ray Neutron Sensor (CRNS) for soil moisture (VWC) with corrections for atmospheric pressure and humidity; field calibrations using reference counts.
  - Rainfall gauges: OTT Pluvio, tipping-bucket gauge (RainE) with wind-corrected measurements.
  - Time-domain reflectometry soil moisture sensors (TDT) at multiple depths for soil moisture and soil temperature.
  - Soil heat flux plates (0.03 m depth).
  - Radiometer (NR01) for net radiation; four-component radiometer for shortwave/longwave components.
  - Automatic weather station with air temperature, humidity, and barometric pressure sensors.
  - PhenoCam for green color content (GCC) imagery in daily granularity.
  - Snow depth sensors and SnowFox for snow-related metrics.
  - Data loggers (Micrologger) and field engineering support; instrumentation has evolved over time and varies by site (see section 7.2 for site-specific setups).
- Site-specific setup variation is documented; some sites have decommissioned sensors or changed configurations over time.

## Changes to data and data processing
- Data are reprocessed when improvements are made; major changes listed (e.g., 2023 corrections to VWC at Hollin Hill, CRNS adjustments, infilling adjustments, precipitation updates, VWC calibration updates).
- Historical changes include VWC recalibration, new gamma/calibration parameters, infilling policy updates, SWE additions, daily albedo incorporation, and method updates for PE and other derived products.

## Data governance, stewardship, and contacts
- Primary author and data steward: S. Stanley; data management and network operations managed by H.M. Cooper, M. Fry, R. Smith, O. Swain, H.C. Ward, among others.
- Site metadata and network configuration contributed by multiple collaborators; data processing algorithms, presentation, analysis, and interpretation contributed by a broad team.
- For data access, inquiries, and stewardship coordination, contact the COSMOS-UK data team through the provided project channels and the NERC EIDC repository.

## Practical considerations for data use and reuse
- Use caution with GCC: daily GCC values are derived from PhenoCam imagery but have not undergone quality control.
- Derived variables (e.g., VWC from CRNS) require understanding of calibration steps (CTS_MOD_CORR, N0_MOD, etc.) and corrections to interpret values properly.
- Data flags are practical for assessing data reliability and infilling status; QC flags identify reasons for data removal and should be consulted for data quality decisions.
- Temporal alignment: sub-hourly data end-of-period timestamps; hourly telemetering and aggregation are described (30-minute to hourly/daily transitions).
- Where updates or corrections occur (data changes), reprocessing ensures consistency across the full time series.

## References and sources
- Stanley et al. 2023 – COSMOS-UK data collection, processing, and documentation (NERC EIDC).
- Methodologies for VWC derivation from cosmic-ray neutron sensors (Evans et al., 2016; Zreda et al., 2012; Franz et al., 2013; Baatz et al., 2014; Köhli et al., 2015).
- Penman-Monteith method for potential evapotranspiration (FAO, 1998; FAO 56).
- Snow and albedo methods for SWE estimation (Wallbank et al., 2020).