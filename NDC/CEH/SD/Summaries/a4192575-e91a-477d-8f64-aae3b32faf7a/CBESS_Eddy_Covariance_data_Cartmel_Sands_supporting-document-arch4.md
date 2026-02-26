# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Cartmel Sands, Morecambe

## Overview
- Dataset of eddy covariance flux measurements at Cartmel Sands, Morecambe, within the CBESS program.
- Time coverage: half-hourly data from 31 May 2013 to 26 January 2015.
- Measurements include CO2 fluxes, energy balance components, meteorology, and soil parameters.
- Data processing includes quality control, gap filling, and flux corrections; data provided in CSV format with detailed metadata.

## Location and Site Context
- Location: Cartmel Sands salt marsh, at the mouth of the Leven estuary in Morecambe.
- Environment: exposed to dominant south-westerly winds; marsh length ~3.2 km, width up to 1 km; features fine sandy sediments and a dentritic creek system; saltmarsh pans present.
- Site scheme includes a lattice tower at ~4.3 m for flux measurements.

## Observations and Data Collection
- Fluxes and wind velocity measured at 10 Hz; half-hourly flux values derived.
- Non-flux variables recorded at 15-minute intervals; mean half-hour values computed.
- Instrumentation: Campbell Scientific CR5000 datalogger; CO2 flux measured with a collocated LI-7500 analyzer and CSAT3 anemometer.
- Calibration and processing: data processed using EdiRe and Matlab; air temperature and humidity converted to vapour pressure deficit (VPD); precipitation measured with EML ARG100 gauge; net radiation and PAR measured with specified sensors.
- Time reference: half-hourly data centered on the interval (e.g., 00:15 is between 00:00 and 00:30).

## Variables Observed or Simulated
- Meteorological: Air temperature (T_air), Soil temperatures (T_soil_5cm, T_soil_10cm), Relative humidity (RH), Net radiation (Net_rad), Photosynthetically active radiation (PAR), Precipitation (Precip), Wind speed (Wind_Spd), Wind direction (Wind_Dir), Vapour pressure deficit (VPD).
- Fluxes and related: CO2 flux (Fc) and filled (Fc_Filled), Latent energy flux (LE) and filled (LE_Filled), Sensible heat flux (H) and filled (H_Filled), u* friction velocity (ustar), Monin-Obukhov stability (MO).
- Quality and modeling: Quality Control flags for LE, Fc, H (LE_QC, Fc_QC, H_QC); Modelled respiration (Resp).

## Instrumentation and Processing Details
- Data collection: 10 Hz fluxes and wind measurements; remaining variables at 15-minute intervals.
- Sensors: LI-7500 CO2 flux sensor, CSAT3, Vaisala MP103A for T and RH, Kipp and Zonen NR Lite for Net Rad, PAR sensor, tipping-bucket rain gauge.
- Data processing: corrections for frequency losses (WPL), storage term correction for CO2, QC-based data selection, radiation-based binning for QC checks, basic reality checks within bins.
- Data handling: fluxes filled using REddyProc gap-filling package, applied to QC = 0 data only; respiration modeled with Lloyd & Taylor (1994) approach, adjusted for tidal depth.

## Quality Control and Gap-Filling
- QC flags: 0 = best, 1 = marginal, 2 = poor, 3 = very poor.
- Data binned by radiation into 15 populated bins; outliers beyond 3.5 SD flagged as QC = 1, beyond 5 SD flagged as QC = 2.
- Data affected by tower wind shadow flagged with QC = 3.
- Gap-filling performed using REddyProc; only QC = 0 data used for filling.
- Respiratory component modeled from nocturnal QC = 0 data, with monthly segmentation and tidal depth adjustments.

## Data Formats and Access
- Primary format: CSV files.
- Comprehensive dataset field descriptions provided; header and row structure documented to support sorting and interpretation.
- Time stamps and seasonal/locational fields included to support cross-site and temporal analyses.

## Data Stewardship, Documentation, and Use
- Detailed methodological documentation covers measurements, calibrations, QC, gap-filling, and modeling steps.
- Metadata supports discovery, traceability, and reproducibility for data leaders planning data strategy, cross-team reuse, and integration into broader data ecosystems.

## Data Quality Considerations and Limitations
- Data gaps due to sensor malfunctions or power loss; clearly indicated in metadata.
- Quality Flags must be considered when using fluxes and derived variables.
- Spatial specificity limited to Cartmel Sands salt marsh; generalization to other sites requires caution.

## Related Metadata and Field Descriptions
- Dataset includes structured field definitions for: Year, Month, Day, Hour, Minute; Location (Morecambe/M), Site (CS, WS, WP); Habitat (Mudflat, Saltmarsh); Quadrat Number; Scale; and variables (T_air, T_soil_5cm, T_soil_10cm, RH, Net_rad, PAR, Precip, Wind_Spd, Wind_Dir, VPD, LE, LE_Filled, LE_QC, Fc, Fc_Filled, Fc_QC, H, H_Filled, H_QC, Resp, ustar, MO).
- Includes descriptive headers for dataset description, cell format, and row numbering to preserve original input order.