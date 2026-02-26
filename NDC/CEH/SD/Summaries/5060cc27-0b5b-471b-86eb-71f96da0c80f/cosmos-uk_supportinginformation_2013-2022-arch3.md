# Supporting documentation for COSMOS-UK. Stanley et al. (2023). Daily and sub-daily hydrometeorological and soil data (2013-2022) [COSMOSUK]. NERC Environmental Information Data Centre.

## Overview
- Describes the COSMOS-UK dataset of daily and sub-daily hydrometeorological and soil moisture observations across 51 sites from 2013 to 2022.
- Comprises 258 files including site metadata, sub-hourly data and flags, daily data and flags, sub-hourly and daily metadata, and author/contributions information.
- Data are sourced from a network of on-site instruments, processed, quality assured, and stored with associated metadata and governance details.

## Data coverage and structure
- Sub-hourly data (30-minute resolution) and daily data (derived metrics) across COSMOS-UK sites.
- Sub-hourly data include grid of variables: radiation (LWIN, LWOUT, SWIN, SWOUT, RN), precipitation (PRECIP, PRECIP_TIPPING, PRECIP_RAINE), meteorology (PA, TA, WS, WD, Q, RH), snow (SNOW_DEPTH), wind components (UX, UY, UZ), heat fluxes (G1, G2), soil temperature and moisture from TDT sensors, soil temperature at multiple depths (STP_TSOIL*), and other derived/auxiliary variables (COSMOS_VWC, SWE, PE, GCC, ALBEDO, GCC from PhenoCam).
- Daily data include net radiation (RN), precipitation components, atmospheric pressure (PA), temperature (TA), wind (WS, WD), humidity (Q, RH), heat fluxes (G1, G2), soil temperature/moisture from TDT sensors, snow metrics (SNOW, SNOW_DEPTH, SWE), Potential Evapotranspiration (PE), albedo, and green colour content (GCC) derived from PhenoCam.
- Data use -9999 to denote missing values; timestamps use ISO 8601; end of 30-minute period is the timestamp for aggregation.
- Metadata files include COSMOS-UK_SiteMetadata_2013-2022.csv with site coordinates, soils, land cover, and decommissioned sites notes.

## Quality control and data governance
- Two-stage quality control (QC):
  - Automatic QC tests with per-variable applicability; failing data are flagged and removed; QC flags stored in COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_QC_Flags.csv with _QCFLAG suffix.
  - Daily visual inspection of data via automatic plots.
- QC flags differentiate why data were removed, enabling traceability of QC decisions.
- QC tests are described in tables 3.2 and 3.3; not all variables undergo QC (e.g., RN and Q are derived from QC’d data and are not themselves QC’d).
- Data flags (COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_Flags.csv) provide information on data quality and infilling status with four flags: M (Missing), U (Unchecked), I (Infilling), E (Estimated).
- Distinction between QC flags (why data were removed) and data flags (nature of data status, e.g., infilled).

## Infilling and data completeness
- Infilling fills gaps using interpolation (Linear or Order-2 Polynomial) for selected variables and reasonable gaps.
- Gap-size rules determine method choice (up to 10-point gaps, surrounding data used; polynomial interpolation used for larger gaps when enough context exists).
- RMSE-based evaluation guides the best interpolation method for each gap and variable.
- Daily data are derived from sub-hourly data and are not independently QC’d; derived data (e.g., VWC, SWE, PE, GCC) inherit QC status from underlying data.
- Completeness indicators per site across Met (meteorological) and Soil groups, plus VWC completeness for CRNS-derived measurements.

## Instrumentation and site variability
- COSMOS-UK uses a suite of instruments with site-to-site variations and time-based changes:
  - Cosmic-Ray Neutron Sensor (CRNS) for volumetric water content (VWC) with counts corrected for atmospheric conditions; multiple methods for deriving VWC (N0-calibration, hmF, or transport models).
  - Rain gauges and tipping-bucket rain gauges for precipitation measurements.
  - Time-domain transmission (TDT) soil moisture and soil temperature sensors at multiple depths.
  - Soil heat flux plates and radiometers for energy balance components.
  - Automatic weather station components for temperature, humidity, and pressure.
  - PhenoCam for GCC (green colour content) derived from images; not quality-controlled in this release.
  - Snow-related sensors and SnowFox for SWE estimation.
- Sections 7.1–7.2 detail instrument types, site setups, and time-varying configurations; some sites have incomplete arrays or decommissioned components noted.

## Data management, changes and authorship
- Changes to data documented (major revisions listed, e.g., 2020–2023 reprocessing, VWC recalibrations, infilling adjustments, gamma corrections for CRNS).
- Major revisions trigger full reprocessing of time series to maintain consistency.
- Primary authorship and management roles are credited; ongoing data processing, site metadata compilation, and network maintenance are described.

## Access and references
- Data are hosted and described for COSMOS-UK at NERC Environmental Information Data Centre.
- References include foundational methodology for VWC derivation from CRNS, calibration approaches, and methodology for deriving SWE, PE, GCC, and other variables.

## Practical implications for monitoring frameworks
- Provides a comprehensive, well-documented data platform with metadata, QC, data flags, and infilling procedures to support policy scrutiny and decision-making.
- Transparent data provenance, quality control reasoning, and data governance (open data, metadata, flagging) facilitate auditing, replication, and cross-site comparisons.
- Acknowledges data gaps, instrumentation heterogeneity, and areas not quality-controlled (e.g., GCC), which are important considerations for interpreting results and decisions based on these data.