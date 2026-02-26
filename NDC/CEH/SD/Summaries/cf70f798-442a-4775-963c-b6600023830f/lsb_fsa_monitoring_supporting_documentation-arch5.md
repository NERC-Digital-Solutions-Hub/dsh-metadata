# Littlestock Brook Flood Storage Area Monitoring Supporting Documentation

## Overview
- Dataset of high-resolution water level data for 9 flood storage areas (FSAs) in the Littlestock Brook catchment (2018–2022).
- Includes raw, atmospheric-corrected, and mean sea level (MASL) adjusted water level data (5-minute resolution), plus estimated stored volume (5-minute resolution) derived from depth-stored volume lookups using a DEM/ LiDAR-based approach.
- Combined atmospheric pressure time-series (1–5-minute resolution) for barometric correction.
- Collected as part of the Littlestock Brook Natural Flood Management (NFM) scheme; funded by the Environment Agency; dataset produced by UKCEH; tied to two NERC-funded PhD projects.
- Contains data gaps due to dry periods or sensor errors; supported by SPITFIRE and SCENARIO NERC DTPs.

## Data Contents
- 9 FSA data files (P1–P9) with 7 columns: Timestamp, Raw_Pressure, Bruen_Pressure, Raw_level, Corrected_level, MASL, FSA_Volume.
- 5 atmospheric pressure files (Bruern_Baro_QC_2018–2022) with 4 columns: Timestamp, Bruern_Pressure, Sensor, Ob_type.
- Site coordinates provided (Table 1) for the 9 FSA monitoring sites and atmospheric pressure monitoring locations.
- Metadata table (Table 3) describing dataset variables and units.
- Documented data structure and units for all fields (e.g., pressure in mbar, water level in mm, MASL in m, FSA_Volume in m³).

## Data Collection and Provenance
- 9 FSA sites monitored in Littlestock Brook south sub-catchment; 5 atmospheric-pressure sites (Grange Farm area) used for barometric corrections.
- Water levels logged with Level TROLL 100 data loggers (5-minute intervals) submerged in stilling wells; stage boards surveyed with RTK-GNSS to convert to mASL.
- Atmospheric pressure recorded with BAROTROLL 100 sensors at Grange Farm; two sensors (Bruern_1 and Bruern_2) with data infilled by LR sensor data when needed.
- Data gaps addressed by infilling with LR data and interpolation where applicable; missing data gaps also flagged via QC.
- DEMs created from 1 m LiDAR (or as-built manual surveys where LiDAR was unavailable) to derive max static water levels and depth-volume relationships; depth-area-volume toolset used to generate per-FSA volume lookups.
- Volume time-series produced by applying depth-volume relationships to corrected water-level time-series.

## Processing, Corrections, and Analytical Methods
- Atmospheric pressure data: missing values infilled using regression Bruern_Pressure = 1.0047144 × Bruern_LR + 6.7531475 (trained on 2018 H2 2018 data; validated 2019).
- Barometric correction: water level corrected with the formula relating raw pressure and atmospheric pressure to produce water level in mm.
- Water level to stage conversion: linear regression per FSA mapping Raw/Corrected levels to stage readings; per-FSA slope, intercept, and mASL offset provided (Table 2).
- FSA volume: derived from depth-stored volume lookup tables based on DEM-derived maximum static water level and connectivity threshold to the stream channel.
- Data structure: files and variables documented in Table 3, including units and whether values are observed or interpolated.

## Data Quality and Quality Control
- Atmospheric pressure QC:
  - Check for missing timestamps and NaNs; fill if needed.
  - Assess differences and outliers; remove implausible values.
  - Regress LR data against Bruern_1 to predict GF pressure; validate against 2019 data; combine Bruern_1/LR/Bruern_2 for continuous time series.
  - Interpolate to 00:05 intervals where necessary.
- Water level QC:
  - Manage gaps during site visits; flag and exclude values when the sensor was out of water or during anomalous periods.
  - Validate against the stage-board regression; inspect for steps, spikes, or negative values; infill when reliable; otherwise remove.
  - Visual checks to identify residual outliers; set remaining implausible values to NA.
- Calibration: sensors factory-calibrated; clock drift checked at each site visit; no significant drift detected.

## Data Structure and File Organization
- FSA data files: P1-QC-Vol, P2-QC-Vol, P3-QC-Vol, P4-QC-Vol, P5-QC-Vol, P6-QC-Vol, P7-QC-Vol, P8-QC-Vol, P9-QC-Vol.
  - Columns: Timestamp; Raw_Pressure; Bruen_Pressure; Raw_level; Corrected_level; MASL; FSA_Volume.
- Barometric pressure files: Bruern_Baro_QC_2018, Bruern_Baro_QC_2019, Bruern_Baro_QC_2020, Bruern_Baro_QC_2021, Bruern_Baro_QC_2022.
  - Columns: Timestamp; Bruern_Pressure; Sensor; Ob_type.
- Metadata: Table 3 describes dataset variables, units, and formats.
- Note: P6 data missing July–October 2020 due to a sensor error.

## Calibration and Units
- Pressure sensors: raw and combined (Bruen) pressure in millibars (mbar); level derived in mm; MASL in meters above mean sea level; FSA_Volume in cubic meters.
- Regression-based corrections and offsets per FSA provided to convert sensor readings to calibrated stage and MASL.

## Known Limitations and Gaps
- Data gaps due to dry periods and sensor errors; one notable gap: P6 missing July–October 2020.
- Some FSAs require bespoke handling due to occasional non-interoperable equipment or limited LiDAR coverage in older sites.

## Reuse, Provenance, and Governance
- Data produced under the Littlestock Brook NFM monitoring program; funded by Environment Agency; coordinated by UKCEH; linked to SPITFIRE and SCENARIO NERC DTPs.
- Documentation provides explicit provenance, methods, and QC steps suitable for data stewardship, auditing, and metadata enhancement.
- Data are organized with explicit QC indicators (Observed vs Interpolated) to support data governance, discovery, and reuse.