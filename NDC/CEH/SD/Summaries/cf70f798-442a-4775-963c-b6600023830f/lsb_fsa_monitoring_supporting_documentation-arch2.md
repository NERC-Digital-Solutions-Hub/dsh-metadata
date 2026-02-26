# Littlestock Brook Flood Storage Area Monitoring Supporting Documentation

## Overview
- A high-resolution dataset of water levels (5-minute), atmospheric-corrected, and mean sea level adjusted for 9 flood storage areas (FSAs) in the Littlestock Brook catchment (tributary of the River Evenlode) covering 2018–2022.
- Includes estimated FSA stored volumes (5-minute) derived from depth-stored volume lookups using a DEM-based approach.
- Includes a combined atmospheric pressure time-series (1–5 minute) used to correct water levels.
- Collected as part of the Littlestock Brook Natural Flood Management (NFM) scheme (a 5-year EA-funded project using低-cost nature-based solutions).
- Data collected by UKCEH as part of a hydrological monitoring programme; interpreted in two NERC-funded PhD projects.
- Some data gaps due to dry FSAs or sensor errors. Support: SPITFIRE DTP and SCENARIO DTP.

## Data collection and study area
- 9 FSA monitoring sites in Littlestock Brook south sub-catchment (headwater of the River Evenlode; upper Thames basin). 8 offline FSAs and 1 online FSA (P1).
- 5 atmospheric-pressure monitoring locations; data primarily from Grange Farm (GF) with two BAROTROLL sensors and Little Rissington (LR) data for infilling.
- Site coordinates provided (Table 1) and displayed in accompanying figures.
- Water levels monitored with Level TROLL 100 loggers; 5-minute sampling; stilling wells to minimise turbulence; stage boards surveyed to 1 cm accuracy using RTK-GNSS for conversion to metres above sea level (mASL).
- Atmospheric pressure recorded with BAROTROLL 100 sensors at GF; Bruern_1 (2018–2019) and Bruern_2 (from 2019); LR data used to infill gaps; data interpolated to 1-minute timestamps where needed.
- FSA storage volumes estimated per FSA using a 1 m LiDAR DEM; where LiDAR was unavailable, manual survey data interpolated using Natural Neighbor.
- DEMs used in ArcGIS to determine maximum static water level; depth-area-volume toolset produced per-FSA lookup tables; volumes derived by matching water levels to these tables.

## Data content and structure
- Nine FSA CSV files: P1-QC-Vol, P2-QC-Vol, P3-QC-Vol, P4-QC-Vol, P5-QC-Vol, P6-QC-Vol, P7-QC-Vol, P8-QC-Vol, P9-QC-Vol (7 columns each).
- Five atmospheric-pressure CSV files: Bruern_Baro_QC_2018, Bruern_Baro_QC_2019, Bruern_Baro_QC_2020, Bruern_Baro_QC_2021, Bruern_Baro_QC_2022 (4 columns each).
- Columns in FSA files: Timestamp; Raw_Pressure; Bruen_Pressure; Raw_level; Corrected_level; MASL; FSA_Volume.
- Columns in barometric files: Timestamp; Bruern_Pressure; Sensor; Ob_type.
- Table 3 (metadata) describes each variable’s units/formats. Units include mbar (pressure), mm (water level), m (MASL), and m^3 (FSA volume).

## Analytical methods
- Atmospheric pressure gaps filled using regression: Bruern Pressure = 1.0047144 × Bruern LR + 6.7531475 (LR = Little Rissington data); trained on 2018 Jul–Dec and tested 2019 Jan–Apr.
- Barometric correction for water level:
  - Water Level (mm) = 1000 × [100 × (Raw_Pressure − Bruern_Pressure)] / (1000 × 9.81).
- Water level corrected to stage via per-FSA linear regression between sensor readings and stage-board measurements; per-FSA slope, intercept, and mASL offset provided (Table 2).
- FSA volumes produced by applying depth-stored-volume lookups to the corrected water levels.
- Data handling includes data infill where confidence is high; otherwise, gaps remain as NA.

## Data quality control and calibration
- Field instrumentation:
  - Level TROLL 100 and BAROTROLL 100 data loggers; factory calibration before deployment; clock drift checked at each site visit (no significant drift observed).
- Atmospheric-pressure QC (BAROTROLL data):
  - Check for missing timestamps; gap-filling with NA where needed.
  - Outlier detection and plausibility checks; regression-based infill using LR data to predict GF pressure when required.
  - Combine Bruern_1, Bruern_LR, and Bruern_2 into a continuous time-series; interpolate to 00:05 intervals.
- Water-level QC (TROLL data):
  - Handle gaps due to log changes or sensor removal; remove implausible values; verify stage-board regression; identify and remove spikes/outliers.
  - Infill Corrected_Level when stage-board readings provide high-confidence estimates; otherwise set to NA.
  - Visual checks for negative values or sensor errors; remove erroneous data.
- Noted data gaps:
  - P6 data missing July–October 2020 due to a sensor error.
- Data precision:
  - Raw and corrected pressures recorded to high precision (mbar); water level in mm; MASL in metres; volumes in cubic metres.

## Instrumentation and calibration
- Instruments:
  - Level TROLL 100 Data Logger (water level).
  - BAROTROLL 100 Data Logger (atmospheric pressure).
- Calibration:
  - Factory calibration for pressure sensors; clock drift checked and deemed insignificant; calibration steps verified via QC checks.

## Limitations and considerations
- Data gaps due to dry FSAs or sensor issues; P6 missing mid-2020; some periods with interpolated data.
- Relative height errors in DEM-based volume estimates are ≤ ±5 cm; absolute height error target by EA is ≤ ±15 cm (RMSE).
- Atmospheric data from multiple sensors are fused with LR data for infilling; accuracy depends on regression performance and LR data availability.

## Access, usage, and metadata
- Data structure includes per-FSA volumes and corrected water levels suitable for monitoring environmental health and flood risk in the Littlestock Brook NFM context.
- Files are named and structured to support traceability (P1–P9 QC Vol files and Bruern_Baro QC files).
- Metadata (Table 3) documents units, formats, and data provenance; data can be stored/uploaded to appropriate portals as part of standard monitoring workflows.

## Funding, collaboration, and scope
- Part of the Littlestock Brook NFM monitoring programme; supported by the Environment Agency, SPITFIRE NERC DTP, and SCENARIO NERC DTP.
- Results underpin long-term environmental monitoring, policy performance evaluation, and broader datasets intended for data reuse and cross-project analyses.