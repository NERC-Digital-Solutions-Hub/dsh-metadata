# Littlestock Brook Flood Storage Area Monitoring Supporting Documentation

## Overview
- High-resolution (5-minute) water level data for 9 flood storage areas (FSAs) in the Littlestock Brook catchment (a tributary of the River Evenlode) from 2018–2022.
- Includes estimated 9 x FSA stored volumes (5-minute resolution) derived from depth-stored volume lookups using a DEM-based model.
- Combined atmospheric pressure time-series (1–5-minute resolution).
- Part of the Littlestock Brook Natural Flood Management (NFM) scheme monitoring; funded by the Environment Agency and linked to two NERC-funded PhD projects.
- Some data gaps due to dry FSAs or sensor errors.

## Datasets and contents
- Nine FSA data files: P1-QC-Vol, P2-QC-Vol, P3-QC-Vol, P4-QC-Vol, P5-QC-Vol, P6-QC-Vol, P7-QC-Vol, P8-QC-Vol, P9-QC-Vol (CSV; seven columns: Timestamp, Raw_Pressure, Bruen_Pressure, Raw_level, Corrected_level, MASL, FSA_Volume).
- Five atmospheric pressure files: Bruern_Baro_QC_2018, Bruern_Baro_QC_2019, Bruern_Baro_QC_2020, Bruern_Baro_QC_2021, Bruern_Baro_QC_2022 (CSV; four columns: Timestamp, Bruern_Pressure, Sensor, Ob_type).
- Metadata: Table 3 describing variables and units (timestamps UTC; pressures in mbar; levels in mm or mASL; volumes in m^3).

## Spatial information and locations
- Monitoring sites located in the Littlestock Brook south sub-catchment, within the upper Thames basin.
- Coordinates provided for all sites (P1–P9, Grange Farm (GF), Little Rissington (LR)) in Table 1 (Latitude/Longitude in decimal degrees).

## Monitoring and instrumentation
- Water level measurement: Level TROLL 100 data loggers (5-minute intervals) submerged in stilling wells; stage boards surveyed to 1 cm accuracy using RTK-GNSS to convert water levels to meters above sea level (mASL).
- Atmospheric pressure measurement: Rugged BAROTROLL 100 sensors at Grange Farm (GF). Two sensors used: Bruern_1 (07/08/2018–15/04/2019) and Bruern_2 (installed 03/07/2019). LR data used to fill gaps (RB: LR data available at 60-minute intervals; interpolated to 1-minute timestamps as needed).
- LiDAR-based DEM (1 m resolution) used to estimate FSA volumes; where LiDAR unavailable, manual survey data interpolated with Natural Neighbor method.

## Data processing workflow (GIS-friendly)
- DEMs used to identify maximum static water level (lowest elevation on the FSA bund) and to generate depth-area-volume lookups for each FSA.
- Continuous water level time-series corrected for barometric pressure and converted to volume via depth-stored lookup tables.
- Atmospheric pressure data quality-controlled and infilled using regression with Little Rissington data (Bruern_LR) to produce continuous GF pressure series.
- Water levels converted from raw pressure to stage using site-specific linear regression (slope, intercept) and datum offsets to produce MASL values; volumes derived from depth-volume relationships.
- Time-series alignment: atmospheric pressure time-series combined from Bruern_1, Bruern_LR, and Bruern_2; water level data corrected and interpolated to 1-minute timestamps where needed (with 00:05 interval adjustments).

## Calibration, QA, and data quality
- Sensors factory-calibrated; clock drift checked at site visits; no significant drift observed.
- QA steps include:
  - Timestamp completeness; NA checks; outlier detection.
  - Regression between Bruern_LR and Bruern_1 to predict GF pressure; consistency checks across periods.
  - Linear regression per FSA to convert raw to corrected water levels; inspection for steps, spikes, missing data.
  - Infill of corrected levels when reliable; removal of data when unreliable.
  - Visual time-series checks for remaining anomalies; NA assignment for negative or erroneous readings.
- Calibration details and regression parameters (slopes, intercepts, and mASL offsets) are provided per FSA (see Table 2).

## Atmospheric pressure handling and regression model
- Missing Bruern data infilled using regression: Bruern Pressure = 1.0047144 × LR Pressure + 6.7531475 (model trained July–December 2018; tested Jan–Apr 2019).
- Pressure corrections applied to water level using the specified barometric correction equation.
- Data quality-control sequence ensures a consistent pressure time-series across all GF barometer data.

## Data structure and access
- File structure:
  - 9 FSA data CSVs: P1-QC-Vol through P9-QC-Vol (each with 7 columns as described).
  - 5 atmospheric pressure CSVs: Bruern_Baro_QC_2018–2022 (columns: Timestamp, Bruern_Pressure, Sensor, Ob_type).
  - Metadata Table 3 describing variable units/formats.
- Timestamps are UTC (YYYY-MM-DD hh:mm:ss); pressures in millibars; water levels in mm (above TROLL) and mASL; volumes in cubic meters.

## Gaps, limitations, and caveats
- Data gaps due to dry FSAs and sensor issues; notable gap: missing P6 data from July–October 2020.
- Absolute height accuracy: ±15 cm RMSE (Earth Agency requirement); relative height error ~±5 cm.
- Volume estimates rely on DEM quality and depth-area-volume lookups; uncertainties propagate to stored volume estimates.
- Some atmospheric pressure data were infilled using LR data; interpolation may introduce additional uncertainty in pressure corrections.

## Practical notes for GIS work
- Suitable for time-series mapping of water levels, pressures, and stored volumes across the 9 FSAs.
- Use the provided MASL offsets per FSA to align water levels to a common vertical datum.
- Integrate FSA_Volume with spatial polygons representing each FSA boundary; apply depth-volume lookups to derive interpolated volumes for visualization.
- Leverage the geospatial coordinates and ArcGIS workflows described (DEM-based volume estimation, maximum static water level) to create georeferenced layers showing stage, pressure, and storage volume over time.

## Provenance and funding
- Data collected by UKCEH as part of the Littlestock Brook NFM monitoring programme.
- Funded by the Environment Agency; SPITFIRE NERC DTP (NE/L002531/1) and SCENARIO NERC DTP (NE/L002566/1) supported related PhD projects.